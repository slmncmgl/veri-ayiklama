# Kylas API — Öğrenilenler ve Devam Planı (v1.0)

Bu dosya, Kylas API'si üzerine yapılan çalışma oturumunun özetidir. Yeni bir oturumda
(ör. "this computer" ortamı) kaldığı yerden devam etmek için gereken her şeyi içerir.

Bu klasördeki dosyalar:
- `KYLAS_OGRENILENLER.md` — bu dosya (öğrenilenler, kararlar, sıradaki adımlar)
- `kylas-api-referans.md` — Postman koleksiyonundan üretilen tam referans (176 endpoint, açıklama + body şablonları)
- `kylas-postman-collection.json` — ham Postman koleksiyonu (kaynak: https://documenter.getpostman.com/view/3365774/UzBiQ8vJ)

> GÜVENLİK: API key ve Bearer token bu dosyalara bilerek YAZILMADI. Key n8n akışında ve
> önceki sohbette açıkta paylaşıldı → Kylas'ta yenilenmeli. Yeni key'i `KYLAS_API_KEY`
> ortam değişkeninde tut.

---

## 1. Genel API kuralları

- Base URL: `https://api.kylas.io/v1` (Reports: `https://api.kylas.io/v3`)
- Auth (ikisinden biri):
  - `api-key: <uuid>:<tenantId>` → n8n / script için bu kullanılır (tenantId = `19886`)
  - `Authorization: Bearer <uuid>:<tenantId>:<userId>` → tarayıcı oturum token'ı, otomasyonda KULLANMA
- `Content-Type: application/json`
- Sayfalama: `?page=0&size=100&sort=updatedAt,desc` → cevapta `content`, `totalElements`, `totalPages`, `last`, `number`
- Picklist / source / tip / durum alanları **metin değil sayısal ID** alır.
  ID'ler: `GET /ui/layouts/CREATE/LEAD`, `GET /entities/{entity}/fields`, `GET /fields/{fieldId}`

## 2. Endpoint kalıpları

| İş | İstek |
|---|---|
| Oluştur | `POST /leads/`, `/deals/`, `/contacts`, `/companies/`, `/tasks/`, `/meetings`, `/call-logs/`, `/emails`, `/quotations/`, `/products`, `/webhooks` |
| Tam güncelle | `PUT /leads/{id}` |
| Kısmi güncelle | `PATCH /leads/{id}` body: `[{ "op": "add"/"replace", "path": "/firstName", "value": ... }]` — **boş alanda `replace` çalışmaz, `add` kullan** |
| Ara | `POST /search/{lead\|deal\|contact\|company}?page=0&size=100&sort=updatedAt,desc` body: `{ fields: [...], jsonRule: {...} }` |
| Aşama değiştir / kapat | `POST /{leads\|deals}/{id}/pipeline-stages/{stageId}/activate` body: `{ reasonForClosing, actualValue }` |
| Lead dönüştür | `POST /leads/{id}/convert` |
| Not / görev / call log / toplantı | `relation` / `relatedTo` içinde `targetEntityType`: `LEAD`, `DEAL`, `CONTACT`, `CALL_LOG`, `MEETING` |
| Not ekle | `POST /notes/relation` body: `{ sourceEntity: { description }, targetEntityId, targetEntityType: "LEAD" }` |
| Smart list'ler | `GET /search-lists/lead?size=100` |
| Tek smart list | `GET /search-lists/lead/{listId}` ⚠️ dokümanda yok, canlıda görüldü |
| Kullanıcı | `GET /users/me`, `GET /users/{id}` |
| Webhook olayları | `LEAD_/DEAL_/CONTACT_` + `CREATED/UPDATED/DELETED` |

Tam liste ve body şablonları: `kylas-api-referans.md`.

## 3. Search `jsonRule` formatı (canlı veriden doğrulandı)

```json
{
  "fields": ["id", "firstName", "phoneNumbers", "source", "utmCampaign", "taskDueOn",
             "latestActivityCreatedAt", "latestNotes", "recordActions", "customFieldValues"],
  "jsonRule": {
    "condition": "AND",
    "valid": true,
    "rules": [
      { "id": "ownerId", "field": "ownerId", "type": "long", "input": "long",
        "operator": "equal", "value": 71981, "group": false },
      { "id": "pipeline", "field": "pipeline", "type": "long",
        "operator": "equal", "value": 31227, "group": false },
      { "id": "pipelineStage", "field": "pipelineStage", "type": "long",
        "operator": "equal", "value": 218701, "group": false },
      { "id": "source", "field": "source", "type": "long",
        "operator": "not_in", "value": [2614514, 2614512, 3005340, 2650986, 2614515], "group": false }
    ]
  }
}
```

- Görülen operatörler: `equal`, `not_in`, `in`, `today`, `multi_field` (serbest metin arama), grup için `and` / `or`
- Kurallardaki diğer anahtarlar (`data`, `property`, `primaryField`, `condition`, `not`, `rules`) canlıda `null` geliyor.
- Tarih operatörünün ("latest activity less than") tam adı HENÜZ BİLİNMİYOR.
- Örnek smart list: `633333` (yukarıdaki 4 kural; içinde latest activity kuralı yok)
- `latestActivityCreatedAt` hiç aktivite yoksa `null` döner. Format: `2022-09-23T07:23:03.027+0000`

## 4. Canlı n8n örneği: "Fortis Etkinlik Kaydı" (Tally → Kylas)

Akış: `Webhook1 (POST /fortis-event-form-2026)` → `Lead Parse` (Code, v10.7) → `Create Lead` → `Create Note`

Doğrulanan bilgiler:
- **Create Lead** body:
  ```json
  {
    "firstName": "...", "lastName": "...",
    "emails": [{ "type": "OFFICE", "value": "x@y.com", "primary": true }],
    "phoneNumbers": [{ "type": "MOBILE", "code": "IE", "dialCode": "+353", "value": "871234567", "primary": true }],
    "source": 3017966, "subSource": "fortis", "ownerId": 72189,
    "pipeline": { "id": 31228, "name": "Fortis Abroad", "stage": { "id": 217289, "name": "New Data" } }
  }
  ```
  - `code` = ISO ülke, `dialCode` = `+` ile alan kodu, `value` = ulusal numara (kodda `libphonenumber-js` ile bölünüyor)
  - `source` sayısal ID (3017966 = Event), `subSource` serbest metin
  - Lead oluşturulurken `pipeline` + `stage` verilebiliyor (ayrı activate çağrısı gerekmiyor)
- **Create Note**: `description` içinde HTML (`<b>`, `<br>`) çalışıyor; `targetEntityId` = Create Lead cevabındaki `id`
- Bilinen ID'ler: Pipeline `31228` Fortis Abroad, Stage `217289` New Data, Owner `72189` Alper Tunga, Source `3017966` Event
- Eksikler: hata çıkışları (`continueErrorOutput`) bağlı değil; mükerrer kontrolü yok; ID'ler sabit kodlu; API key node'larda düz metin

## 5. Mevcut proje: "Old Lead" bayrağı

### Amaç
Danışmanların smart list'lerinde, **son N günde (4–5) iletişime geçilmemiş** (hiç aktivitesi
olmayanlar dahil) lead sayısını **Kylas ekranında** görmek. Kylas filtresi "latest activity
less than" sadece sabit tarih alıyor, kayan pencere ("son 5 gün") desteklemiyor.

### Karar verilen çözüm
Sayıyı n8n'de hesaplayıp lead'e **"Old Lead" (yes/no toggle custom field)** olarak yazmak.
Sonra Kylas'taki her smart list'e `Old Lead = Yes` filtresi eklenir → liste sayısı = istenen sayı.

- Bayrak **lead bazlı**, liste bazlı değil. Kapsam: belirli pipeline aşamalarındaki tüm lead'ler.
- n8n her sabah **tek akış** olarak çalışır, danışmanları sırayla işler (5 dk aralıklı ayrı akışlara gerek yok).
- Sadece değeri değişmesi gereken lead'ler PATCH'lenir.

### Planlanan n8n akışı
1. Schedule Trigger (her sabah)
2. Danışman owner ID listesi
3. Her danışman için `POST /search/lead` (ownerId + ilgili pipeline/aşamalar), fields:
   `id`, `latestActivityCreatedAt`, `customFieldValues`; sayfalama `last: true` olana kadar
4. Code node (v1.0): `latestActivityCreatedAt == null` VEYA `< bugün − N gün` → hedef `true`, değilse `false`;
   sadece mevcut değerden farklı olanları geçir
5. `PATCH /leads/{id}` → `[{ "op": "add", "path": "/customFieldValues/<alanAdı>", "value": true }]` + Wait
6. (Opsiyonel) danışman başına özet

### Açık konular / riskler
- **TEST EDİLECEK:** Custom field'ı PATCH etmek `latestActivityCreatedAt`'i değiştiriyor mu?
  Değiştiriyorsa yaklaşım çöker. Test lead'i: **45421669**. Test prompt'u aşağıda.
- **Geri dönüş (Yes → No):** Kullanıcı Kylas otomasyonu ile yapmayı düşünüyor
  ("latest activity is known → Old Lead = No"). ⚠️ Bu koşul geçmişte aktivitesi olan her lead
  için doğru, ve n8n'in PATCH'i "lead updated" olayını tetikleyip bayrağı hemen No'ya çevirir.
  Öneri: otomasyonu aktivite olaylarına (call log / note / task / meeting oluşturuldu) bağla;
  olmazsa bayrağı iki yönlü n8n yönetsin.
- Lead güncellemeleri `LEAD_UPDATED` webhook'larını / bildirimleri tetikleyebilir — kontrol et.
- Netleşecek: Old Lead alanının teknik adı (ör. `cfOldLead`), N = 4 mü 5 mi, kapsamdaki pipeline/aşama ID'leri,
  danışman owner ID'leri, "N gün" = N×24 saat mi takvim günü mü.

## 6. Test prompt'u ("this computer" oturumu için)

```
Kylas CRM API'sinde bir test yapmanı istiyorum. Komutları terminalde sen çalıştır, sonuçları özetle.

AMAÇ
Bir lead'in custom field'ını (Old Lead, yes/no toggle) API ile güncellemenin, o lead'in
"latestActivityCreatedAt" değerini değiştirip değiştirmediğini öğrenmek.

BİLGİLER
- Base URL: https://api.kylas.io/v1
- Header: api-key: $KYLAS_API_KEY   (key'i ortam değişkeninden al; yoksa bana sor)
- Test lead ID: 45421669  (önemsiz test lead'i)

KURALLAR
- SADECE 45421669 ID'li lead'e yazma işlemi yap. Başka hiçbir kayda dokunma.
- Test bitince alanı mutlaka eski değerine geri döndür.

ADIMLAR
1. GET /leads/45421669 → before.json; latestActivityCreatedAt, updatedAt, customFieldValues göster.
2. "Old Lead" alanının teknik adını bul (customFieldValues'da yoksa
   GET /entities/lead/fields?entityType=lead&custom-only=true&page=0&size=100).
   Mevcut değerini not et.
3. PATCH /leads/45421669, Content-Type: application/json-patch+json,
   body [{"op":"add","path":"/customFieldValues/<ALAN_ADI>","value":true}]
   (hata → application/json dene → "replace" dene; ham hatayı göster)
4. 5 sn bekle, GET → after.json; latestActivityCreatedAt / updatedAt / alan değeri önce-sonra tablosu.
5. Alanı eski değerine döndür ve doğrula.

RAPOR: alan teknik adı + tipi, çalışan PATCH formatı, latestActivityCreatedAt değişti mi,
updatedAt değişti mi, geri dönüş başarılı mı, hatalar.
```

## 7. Kullanıcı tercihleri (yeni oturumda da geçerli)

- Sormadan kod yazma; önce çözüm mimarisini anlat, onay al.
- Her kod / script'e versiyon numarası ver, her güncellemede artır (v1.0 → v1.1).
- Kod değişikliğinde silinecek bloğu `// SİL: ...` ile açıkça belirt.
- Cevaplar Türkçe, madde işaretli, ana öneri kalın, gerekçe sonda kısa.
