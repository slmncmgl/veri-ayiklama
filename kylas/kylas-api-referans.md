# Kylas API Referansı (Postman koleksiyonundan)

Base URL: https://api.kylas.io/v1  · Header: `api-key: <KEY>` veya `Authorization: Bearer <token>` · `Content-Type: application/json`

## Lead APIs

#### Create Lead
`POST https://api.kylas.io/v1/leads/`

Create Lead API creates Lead with  required values as below. Review below snippet and set values are per your requirement, Whichever value is not required, set null
API KEY can be found here
Find Ids as below:

For pipeline id and stage ids visit here
For any form field details like picklist value ids, Company type ids, Campaign, Source, any Custom fields and their value ids visit here
For product details and its ids visit here

Sample response below:
{
    "createdAt": "2022-08-08T13:43:02.157+0000",
    "updatedAt": "2022-08-08T13:43:02.157+0000",
    "createdBy": 21,
    "updatedBy": 21,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": true,
        "call": true,
        "sms": true,
        "task": true,
        "note": true,
        "meeting": true,
        "document": false,
        "deleteAll": true,
        "quotation": false
    },
    "metaData": {
        "idNameStore": {
            "newCheckbox": {},
            "country": {},
            "convertedBy": {},
            "updatedBy": {
                "21": "Selldo Kireeti"
            },
            "timezone": {},
            "requirementCurrency": {},
            "source": {},
            "ownerId": {
                "21": "Selldo Kireeti"
            },
            "companyEmployees": {},
            "cfCustomPicklist": {},
            "companyBusinessType": {},
            "importedBy": {},
            "pipeline": {},
            "cfCheckBoxFilterabl

```json
{
    "firstName": "<Enter Lead's First Name>",
    "lastName": "<Emter Lead's Last Name>",
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "value": "9090909091",
            "dialCode": "+91",
            "primary": true
        },
        {
            "type": "MOBILE",
            "code": "IN",
            "value": "9191919191",
            "dialCode": "+91",
            "primary": false
        }
    ],
    "salutation": null,
    "emails": [
        {
            "type": "OFFICE",
            "value": "EnterleadsEmail@domain.com",
            "primary": true
        },
        {
            "type": "OFFICE",
            "value": "EnterleadsSecondaryEmail@domain.com",
            "primary": false
        }
    ],
    "timezone": "Etc/GMT+12",
    "city": "<Lead's City>",
    "state": "<Lead's State>",
    "zipcode": "<Lead's Zipcode>",
    "country": "IN",
    "department": "<Enter Department>",
    "dnd": false,
    "facebook": "https://www.facebook.com",
    "twitter": "https://www.twitter.com",
    "linkedIn": "https://www.linkedin.com",
    "address": "<Lead's address>",
    "companyName": "<Lead's Company>",
    "designation": "Manager",
    "companyAddress": "<Company address>",
    "companyCity": "<Company City>",
    "companyState": "<Company State>",
    "companyZipcode": "<Company Zipcode>",
    "companyCountry": "IN",
    "companyEmployees": null,
    "companyAnnualRevenue": 10000000,
    "companyWebsite": "https://www.companywebsite.com",
    "companyPhones": [
        {
            "type": "MOBILE",
            "code": "IN",
            "value": "9090909090",
            "dialCode": "+91",
            "primary": true
        }
    ],
    "companyIndustry": "BIOTECHNOLOGY",
    "companyBusinessType": "competitor",
    "requirementName": "<Lead's requirement>",
    "requirementCurrency": "INR",
    "requirementBudget": 3500000,
    "products": [
        {
            "id": 18806,
            "name":"Rent Office Space 5000 Sqft"
        }
    ],
    "campaign": null,
    "source": null,
    "customFieldValues": {}
}
```

#### Update Lead
`PUT https://api.kylas.io/v1/leads/<enter_lead_id>`

Update lead currently is a PUT request and It is a 3 step process for now

Fetch lead details using 'Get lead details' API.
From above request's response, update those fields which you want.
Copy paste the new payload in Update lead request's body and hit 'Send' request.

API KEY can be found here
Find Ids as below:

For pipeline id and stage ids visit here
For any form field details like picklist value ids, Company type ids, Campaign, Source, any Custom fields and their value ids visit here
For product details and its ids visit here

Sample response
{
    "createdAt": "2022-08-08T10:29:18.585+0000",
    "updatedAt": "2022-09-23T07:23:03.099+0000",
    "createdBy": 10224,
    "updatedBy": 10224,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": true,
        "call": true,
        "sms": true,
        "task": true,
        "note": true,
        "meeting": true,
        "document": true,
        "deleteAll": true,
        "quotation": false
    },
    "metaData": {
        "idNameStore": {
            "country": {},
            "convertedBy": {},
            "updatedBy": {
                "10224": "full details bardo and convert"
            },
            "timezone": {},
            "requirementCurrency": {},
            "source": {
                "489124": "Google"
            },
            "ownerId": {
                "10323": "test account user"
            },
            "companyEmployees": {
                "48

```json
{
    "salutation": 489111,
    "firstName": "Rohit",
    "lastName": "Sharma",
    "pipeline": {
        "id": 6298,
        "name": "Default Lead Pipeline",
        "stage": {
            "id": 42512,
            "name": "Open"
        }
    },
    "emails": [
        {
            "type": "OFFICE",
            "value": "rohit@gmail.com",
            "primary": true
        }
    ],
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "dialCode": "+91",
            "value": "9090909090",
            "primary": true
        }
    ],
    "timezone": "Asia/Calcutta",
    "address": "<Lead's address>",
    "city": "<Lead's city>",
    "state": "<Lead's state>",
    "country": "IN",
    "zipcode": "411033",
    "facebook": "https://www.fb.com",
    "twitter": "https://www.ty.com",
    "linkedIn": "https://www.li.com",
    "companyName": "Infotech pvt ltd",
    "department": "Engineering",
    "designation": "Lead",
    "companyIndustry": "COMPUTER_SOFTWARE",
    "companyBusinessType": "competitor",
    "companyEmployees": 489119,
    "companyAnnualRevenue": 100000000,
    "companyWebsite": "https://www.infotech.com",
    "companyPhones": [
        {
            "type": "MOBILE",
            "code": "IN",
            "dialCode": "+91",
            "value": "9191919191",
            "primary": true
        }
    ],
    "companyAddress": "Infotech pvt ltd, Andheri West",
    "companyCity": "Mumbai",
    "companyState": "Maharashtra",
    "companyCountry": "IN",
    "companyZipcode": "411033",
    "requirementName": "Office Space",
    "products": [
        {
            "id": 39010,
            "name": "Rent Office Space 5000 Sqft"
        }
    ],
    "requirementCurrency": "INR",
    "requirementBudget": 400000,
    "campaign": 489123,
    "source": 489124,
    "customFieldValues": {}
}
```

#### Update lead patch
`PATCH https://api.kylas.io/v1/leads/{{Lead_Id}}`

```json
[
      // Note: Replace operation can only be performed if the field already exists. 
// If the field is empty or not initialized, use "add" operation instead.

      {
        "op": "add",
        "path": "/ownerId",
        "value": 11622
    }, // Owner of the Lead


    //Salutation 
    // Salutation of Lead (Mr., Ms., Miss., etc.)
    {
        "op": "replace",
        "path": "/salutation",
        "value": 572572
    },
    //Last_Name 
    {
        "op": "add",
        "path": "/lastName",
        "value": "last Name Patch"
    },
    //first_Name 
    {
        "op": "add",
        "path": "/firstName",
        "value": "First name Patch"
    },
    // Email
    // Note: You can not perform replace opration if the Email field is empty 
    {
        "op": "add",
        "path": "/emails/0",
        "value": {
            "type": "OFFICE",
            "value": "user1patch@flexvio.com",
            "primary": false
        }
    },
    {
        "op": "replace",
        "path": "/emails/1",
        "value": {
            "type": "OFFICE",
            "value": "patchuser@flexvio.com",
            "primary": true
        }
    },
    //PhoneNumber
    // Note: You can not perform replace opration if the phone number field is empty 
    {
        "op": "add",
        "path": "/phoneNumbers/0",
        "value": {
            "id": null,
            "type": "MOBILE",
            "code": "IN",
            "value": "8734523499",
            "dialCode": "+91",
            "primary": true
        }
    },
    {
        "op": "add",
        "path": "/phoneNumbers/1",
        "value": {
            "id": null,
            "type": "MOBILE",
            "code": "IN",
            "value": "8734523487",
            "dialCode": "+91",
            "primary": false
        }
    },
    //Pipeline 
    {
        "op": "add",
        "path": "/pipeline",
        "value": {
            "id": 7042,
            "name": "Default Deal Pipeline ",
            "stage": {
                "id": 44240,
                "name": "Prospect/Contacted"
            }
        }
    },
    //Timezone
    {
        "op": "replace",
        "path": "/timezone",
        "value": "Asia/Calcutta"
    },
    //Campign_Information
    {
        "op": "replace",
        "path": "/source",
        "value": 572585
    },
    {
        "op": "add",
        "path": "/campaign",
        "value": 572646
    },
    {
        "op": "add",
        "path": "/subSource",
        "value": "updated by patch subSource"
    },
    {
        "op": "add",
        "path": "/utmSource",
        "value": "updated by patch utmSource"
    },
    {
        "op": "add",
        "path": "/utmCampaign",
        "value": "updated by patch utmCampaign"
    },
    {
        "op": "replace",
        "path": "/utmMedium",
        "value": "updated by patch utmMedium"
    },
    {
        "op": "replace",
        "path": "/utmContent",
        "value": "updated by patch utmContent"
    },
    {
        "op": "add",
        "path": "/utmTerm",
        "value": "updated by patch utmTerm"
    },
    //Social
    {
        "op": "replace",
        "path": "/facebook",
        "value": "http://patchupdatefacebook.com"
    },
    {
        "op": "add",
        "path": "/twitter",
        "value": "http://patchupdatetwitter.com"
    },
    {
        "op": "replace",
        "path": "/linkedIn",
        "value": "http://patchupdatelinkedin.com"
    },
    //Location
    {
        "op": "add",
        "path": "/address",
        "value": "Address field"
    },
    {
        "op": "replace",
        "path": "/city",
        "value": "pune"
    },
    {
        "op": "replace",
        "path": "/state",
        "value": "MH"
    },
    {
        "op": "replace",
        "path": "/zipcode",
        "value": "412410"
    },
    //DND 
    {
        "op": "replace",
        "path": "/dnd",
        "value": false
    },
    //Custom_Fields
    // Note: You can not perform replace opration if the  field is empty 
    {
        "op": "replace",
        "path": "/customFieldValues/cfTextField",
        "value": "updated by patch"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfParagraphText",
        "value": "Add paragraph  description"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfNumber",
        "value": 13
    },
    {
        "op": "replace",
        "path": "/customFieldValues/cfUrlField",
        "value": "https://app.kylas.io/"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfDate",
        "value": "2023-12-13T06:30:00.000Z"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfCheckbox",
        "value": true
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfDateTimePicker",
        "value": "2023-12-13T11:30:00.000Z"
    },
    //Multivalue_Custom_Picklist 
    // Note: 
    //1.When adding Multipicklist Value first time You have to intialise with empty array
    //2.When values is already added then dont intialise with empty array
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiPickList",
        "value": []
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiPickList/0",
        "value": 572637
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiPickList/1",
        "value": 572638
    },
    {
        "op": "replace",
        "path": "/customFieldValues/cfPickList",
        "value": 572620
    },
    //Professional_Details
    // Note: You can not perform replace opration if the Company  phone number field is empty 
    {
        "op": "add",
        "path": "/companyPhones/0",
        "value": {
            "type": "MOBILE",
            "code": "IN",
            "primary": false,
            "value": "8788879898"
        }
    },
    {
        "op": "remove",
        "path": "/companyAnnualRevenue",
        "value": 13678
    },
    {
        "op": "add",
        "path": "/companyWebsite",
        "value": "https://app.kylas.io/"
    },
    {
        "op": "add",
        "path": "/designation",
        "value": "Product engineer "
    },
    {
        "op": "add",
        "path": "/department",
        "value": "engineering "
    },
    {
        "op": "add",
        "path": "/companyState",
        "value": "Maharashtra "
    },
    {
        "op": "add",
        "path": "/companyAddress",
        "value": "4th Floor, Sr. No. 9, H.No:1/2 Near Ramada Plaza, above Maruti Suzuki Suman Kirti Cars Pvt. Ltd, Mahalunge, Pune, Maharashtra 411045 "
    },
    {
        "op": "add",
        "path": "/companyCity",
        "value": "Pune "
    },
    {
        "op": "add",
        "path": "/companyZipcode",
        "value": "411012 "
    },
    {
        "op": "replace",
        "path": "/companyEmployees",
        "value": 572581
    },
    {
        "op": "replace",
        "path": "/companyBusinessType",
        "value": "investor"
    },
    {
        "op": "replace",
        "path": "/companyIndustry",
        "value": "ACCOUNTING"
    },
    {
        "op": "replace",
        "path": "/companyCountry",
        "value": "AD"
    },
    //Requirement
    // Note: You can not perform replace opration if the Product  field is empty 
    {
        "op": "add",
        "path": "/products/0",
        "value": {
            "id": 23540,
            "name": "2 Bhk ",
            "quantity": 1,
            "discount": {
                "value": 0,
                "type": "PERCENTAGE"
            }
        }
    },
    {
        "op": "add",
        "path": "/requirementName",
        "value": "Sales CRM  "
    },
    {
        "op": "add",
        "path": "/requirementBudget",
        "value": 1000
    },
    {
        "op": "add",
        "path": "/requirementCurrency",
        "value": "USD"
    }
]
```

#### Get Lead details
`GET https://api.kylas.io/v1/leads/<enter_lead_id>`

Get lead details API will fetch all the lead details.
API KEY can be found here
Enter lead_id in request URL whose details are to be fetched.
Sample response snippet below:
{
    "createdAt": "2022-07-19T15:09:43.073+0000",
    "updatedAt": "2022-08-08T12:34:41.818+0000",
    "createdBy": 1,
    "updatedBy": 1,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": true,
        "call": true,
        "sms": true,
        "task": true,
        "note": true,
        "meeting": true,
        "document": true,
        "deleteAll": true,
        "quotation": false
    },
    "metaData": {
        "idNameStore": {
            "country": {},
            "convertedBy": {},
            "updatedBy": {
                "1": "Tenant User"
            },          
            "timezone": {},
            "requirementCurrency": {},
            "source": {
                "698": "Google"
            },
            "ownerId": {
                "1": "Tenant User"
            },
            "companyEmployees": {
                "10890": "250-499"
            },
            "companyBusinessType": {},
            "pipeline": {
                "1": "Default Lead Pipeline"
            },
            "createdBy": {
                "1": "Tenant User"
            },
            "campaign": {
                "697": "Organic"
            },
            "companyCountry": {},
            "salutation": {
                "694": "Mr"
            },
      

#### Fetch all Lead pipelines
`GET https://api.kylas.io/v1/pipelines/search?sort=updatedAt,desc&page=0&size=10`

Fetch lead pipelines using this API.
Sample response below
{
    "last": true,
    "first": true,
    "totalPages": 1,
    "size": 10,
    "number": 0,
    "numberOfElements": 6,
    "totalElements": 6,
    "sort": [
        {
            "direction": "DESC",
            "property": "updatedAt",
            "ignoreCase": false,
            "nullHandling": "NATIVE",
            "descending": true,
            "ascending": false
        }
    ],
    "content": [
        {
            "name": "New lead pipeline Digicop",
            "entityType": "LEAD",
            "active": true,
            "id": 1079,
            "recordActions": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": true,
                "updateAll": true,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "name": "pre sales pipeline",
            "entityType": "LEAD",
            "active": false,
            "id": 922,
            "recordActions": {
                "read": true,
                "write": false,
                "update": true,
                "delete": false,
                "email": false,
                "c

```json
{
    "fields": [
        "name",
        "entityType",
        "active",
        "id",
        "recordActions",
        "customFieldValues"
    ],
    "jsonRule": null
}
```

#### Fetch Particular Lead pipeline details
`POST https://api.kylas.io/v1/leads/<enter_lead_id>`

Fetch particular lead pipeline details using this API.
Pipeline id can be found either from pipeline details page URL
or you can fetch list of pipelines using Fetch pipelines API
Sample response below
{
    "createdAt": "2021-03-15T05:20:36.056+0000",
    "updatedAt": "2021-03-15T05:21:48.753+0000",
    "createdBy": 1,
    "updatedBy": 1,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": false,
        "call": false,
        "sms": false,
        "task": false,
        "note": false,
        "meeting": false,
        "document": false,
        "deleteAll": false,
        "quotation": false
    },
    "metaData": {
        "idNameStore": {
            "updatedBy": {
                "1": "Gaurav Pasaarkar"
            },
            "createdBy": {
                "1": "Gaurav Pasaarkar"
            },
            "ownerId": {
                "1": "Gaurav Pasaarkar"
            }
        }
    },
    "id": 1079,
    "name": "New lead pipeline Digicop",
    "entityType": "LEAD",
    "unqualifiedReasons": ["Budget does not match", "False enquiry", "Wrong number", "Customer already bought the product/service", "Bought product/service with competitor", "Did not pick phone", "Not interested anymore", "Duplicate Customer"],
    "lostReasons": ["No followup", "Not interested", "Booked with competitor", "Not answering/responding", "Bought product/service with competitor", "Low budget", "Postponed the decision of buying product/

```json
{
    "fields": [
        "name",
        "entityType",
        "active",
        "id",
        "recordActions",
        "customFieldValues"
    ],
    "jsonRule": null
}
```

#### Change Lead Pipeline Stage
`POST https://api.kylas.io/v1/leads/<enter_lead_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Change Lead pipeline stage from any stage to any stage.
Fetch Pipeline and stage Ids from here
Pipelines can also be fetched by using Fetch lead pipelines API
Sample response below:
{
    "id": 1,
    "name": "Default Lead Pipeline",
    "unqualifiedReasons": ["Budget does not match", "False enquiry", "Wrong number", "Customer already bought the product/service", "Bought product/service with competitor", "Did not pick phone", "Not interested anymore", "Duplicate Customer"],
    "lostReasons": ["No followup", "Not interested", "Booked with competitor", "Not answering/responding", "Bought product/service with competitor", "Low budget", "Postponed the decision of buying product/service"],
    "stages": [{
        "id": 1,
        "name": "Open",
        "description": "When someone fills a form on your website, calls your company number, initiates a chat on your website, or interacts with you on social media and you have not got any specific information related to their requirement/budget to qualify for further stages, it's called Open Lead. \n\nOpen Leads are those you have interacted or not interacted and just received basic details, with no specific requirement from the lead.",
        "forecastingType": "OPEN",
        "position": 1,
        "status": "COMPLETED",
        "startedAt": "2022-08-08T12:32:32.661Z",
        "completedAt": "2022-08-08T13:25:13.312Z",
        "reason": null,
        "winLikelihood": 0
    }, {
        "id": 5682,
        "name": "Prospect/Contacte

```json
{
    "reasonForClosing": null,
    "actualValue": null
}
```

#### Search Lead
`POST https://api.kylas.io/v1/search/lead?sort=updatedAt,desc&page=0&size=100`

Search API searches for a Lead based on the search key value. Search key value can be any of below:

Lead Name (both first name and last name)
Lead Phone number
Lead Email
Lead Company Name

Replace the value  with the desired search keyword in below JSON
Sample response
{
    "content": [],
    "metaData": {},
    "last": true,
    "totalPages": 0,
    "totalElements": 0,
    "first": true,
    "sort": [{
        "direction": "DESC",
        "property": "updatedAt",
        "ignoreCase": false,
        "nullHandling": "NATIVE",
        "descending": true,
        "ascending": false
    }],
    "numberOfElements": 0,
    "size": 10,
    "number": 0
}

```json
{
    "fields": [
        "firstName",
        "lastName",
        "ownerId",
        "pipelineStage",
        "phoneNumbers",
        "pipelineStageReason",
        "createdAt",
        "updatedAt",
        "utmSource",
        "utmCampaign",
        "utmMedium",
        "utmContent",
        "utmTerm",
        "id",
        "recordActions",
        "customFieldValues"
    ],
    "jsonRule": {
        "rules": [
            {
                "id": "multi_field",
                "field": "multi_field",
                "type": "multi_field",
                "input": "multi_field",
                "operator": "multi_field",
                "value": "lead"
            }
        ],
        "condition": "AND",
        "valid": true
    }
}
```

#### Get Lead Form Fields
`GET https://api.kylas.io/v1/ui/layouts/CREATE/LEAD`

This API fetches all system and custom lead form fields
API KEY can be found here
Sample response
{
    "layoutItems": [{
            "type": "SECTION",
            "layoutItems": [{
                    "type": "FIELD",
                    "layoutItems": [],
                    "item": {
                        "id": 4,
                        "sectionId": 1,
                        "type": "PICK_LIST",
                        "entity": null,
                        "displayName": "Salutation",
                        "internalName": "salutation",
                        "pickLists": [{
                                "id": 694,
                                "displayName": "Mr",
                                "name": "MR",
                                "lookupUrl": null,
                                "systemDefault": false,
                                "disabled": false
                            },
                            {
                                "id": 695,
                                "displayName": "Mrs",
                                "name": "MRS",
                                "lookupUrl": null,
                                "systemDefault": false,
                                "disabled": false
                            },
                            {
                                "id": 696,
                                "displayName": "Miss",
                                "name": "MISS",
                                "looku

#### Create Call log on Lead
`POST https://api.kylas.io/v1/call-logs/`

This API is used to create call log on lead
Sample request payload:
'outcome' key can have values 'connected', 'missed', 'rejected', 'busy' and 'no_answer'
For all the above types other than connected, remove 'duration' key
{
    "outcome": "connected",
    "startTime": "2022-09-05T06:56:29.695Z",
    "phoneNumber": "9618488578",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "id": 297573,
        "entity": "lead",
        "phoneNumber": "9618488578"
    },
    "callRecording": {
        "fileName": "call.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}

```json
{
    "outcome": "connected",
    "startTime": "2022-09-05T06:56:29.695Z",
    "phoneNumber": "9618488578",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "id": 297573,
        "entity": "lead",
        "phoneNumber": "9618488578"
    },
    "callRecording": {
        "fileName": "call.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}
```

#### Close Lead as WON
`POST https://api.kylas.io/v1/leads/<Enter_lead_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Close the lead as won using this API
Fetch Pipeline and stage Ids from here

```json
{
    "reasonForClosing": null,
    "actualValue": null
}
```

#### Close Lead as Unqualified
`POST https://api.kylas.io/v1/leads/<Enter_lead_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Close lead as Unqualified using this API.
Fetch Pipeline and stage Ids from here

```json
{
    "reasonForClosing": "Not interested anymore",
    "actualValue": null
}
```

#### Close Lead as Lost
`POST https://api.kylas.io/v1/leads/<Enter_lead_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Close lead as Lost using this API
Fetch Pipeline and stage Ids from here

```json
{
    "reasonForClosing": "Low budget",
    "actualValue": null
}
```

#### Reassign Lead
`PUT https://api.kylas.io/v1/leads/{{lead_id}}/owner`

Reassign lead to other user with this API.
Users ID can be found here
Sample request payload
{
    "ownerId": 102
}

```json
{
    "ownerId": {{owner_id}}
}
```

#### Create Webhook for Lead Create Delete Update
`POST https://api.kylas.io/v1/webhooks`

```json
{
    "name": "lead webhook for create update and delete",
    "requestType": "POST",
    "url": "https://webhookurl.com",
    "authenticationType": "NONE",
    "authenticationKey": null,
    "events": [
        "LEAD_CREATED",
        "LEAD_UPDATED",
        "LEAD_DELETED"
    ],
    "active": true
}
```

#### Convert Lead to Deal, Contact Company
`POST https://api.kylas.io/v1/leads/{{lead_id}}/convert`

Convert the lead to deal, contact and company using this API
Sample payload below:
{
    "deal": {
        "mode": "CREATE",
        "details": {
            "ownedBy": {
                "id": 305
            },
            "estimatedValue": {
                "currencyId": 431,
                "value": 200
            },
            "name": "lead to deal convert"
        }
    },
    "contact": {
        "mode": "CREATE",
        "details": {
            "firstName": "lead to contact",
            "lastName": "convert",
            "phoneNumbers": [
                {
                    "type": "MOBILE",
                    "code": "IN",
                    "value": "9703059348",
                    "dialCode": "+91",
                    "primary": true
                }
            ],
            "emails": [
                {
                    "type": "OFFICE",
                    "value": "email@gmail.com",
                    "primary": true
                }
            ]
        }
    },
    "company": {
        "mode": "CREATE",
        "details": {
            "annualRevenue": {
                "currencyId": 431
            },
            "name": "company from lead convert"
        }
    }
}

```json
{
    "deal": {
        "mode": "CREATE",
        "details": {
            "ownedBy": {
                "id": 305
            },
            "estimatedValue": {
                "currencyId": 431,
                "value": 200
            },
            "name": "lead to deal convert"
        }
    },
    "contact": {
        "mode": "CREATE",
        "details": {
            "firstName": "lead to contact",
            "lastName": "convert",
            "phoneNumbers": [
                {
                    "type": "MOBILE",
                    "code": "IN",
                    "value": "9703059348",
                    "dialCode": "+91",
                    "primary": true
                }
            ],
            "emails": [
                {
                    "type": "OFFICE",
                    "value": "email@gmail.com",
                    "primary": true
                }
            ]
        }
    },
    "company": {
        "mode": "CREATE",
        "details": {
            "annualRevenue": {
                "currencyId": 431
            },
            "name": "company from lead convert"
        }
    }
}
```

#### Convert Lead to Deal
`POST https://api.kylas.io/v1/leads/{{lead_id}}/convert`

Use this API to convert lead to deal
Sample payload:
{
    "deal": {
        "mode": "CREATE",
        "details": {
            "ownedBy": {
                "id": 305
            },
            "estimatedValue": {
                "currencyId": 431,
                "value": 300
            },
            "name": "lead to deal"
        }
    }
}
Sample response below:
{
    "ownerId": 305,
    "convertedAt": "2022-09-05T08:39:50.073+0000",
    "convertedBy": 305,
    "metaData": {
        "idNameStore": {
            "country": {},
            "convertedBy": {
                "305": "Automation user"
            },
            "updatedBy": {
                "305": "Automation user"
            },
            "timezone": {},
            "requirementCurrency": {},
            "source": {},
            "ownerId": {
                "305": "Automation user"
            },
            "companyEmployees": {},
            "companyBusinessType": {},
            "importedBy": {},
            "pipeline": {},
            "createdBy": {
                "305": "Automation user"
            },
            "companyCountry": {},
            "campaign": {},
            "salutation": {},
            "pipelineStage": {},
            "cfCustomPiclist": {},
            "companyIndustry": {}
        }
    },
    "conversionDetails": [
        {
            "entityType": "DEAL",
            "entityId": 25690
        }
    ]
}

```json
{
    "deal": {
        "mode": "CREATE",
        "details": {
            "ownedBy": {
                "id": 305
            },
            "estimatedValue": {
                "currencyId": 431,
                "value": 300
            },
            "name": "lead to deal"
        }
    }
}
```

#### Convert Lead to Contact
`POST https://api.kylas.io/v1/leads/{{lead_id}}/convert`

Convert lead into contact using this API
Sample payload
{
    "contact": {
        "mode": "CREATE",
        "details": {
            "firstName": "1662338177160",
            "lastName": "lasname_87",
            "emails": [
                {
                    "type": "OFFICE",
                    "value": "email@gmail.com",
                    "primary": true
                }
            ],
            "phoneNumbers": [
                {
                    "type": "MOBILE",
                    "code": "IN",
                    "dialCode": "+91",
                    "value": "8080808080",
                    "primary": true
                }
            ],
            "timezone": null
        }
    }
}
Sample response
{
    "ownerId": 305,
    "convertedAt": "2022-09-05T08:48:08.928+0000",
    "convertedBy": 305,
    "metaData": {
        "idNameStore": {
            "country": {},
            "convertedBy": {
                "305": "Automation user"
            },
            "updatedBy": {
                "305": "Automation user"
            },
            "timezone": {},
            "requirementCurrency": {},
            "source": {},
            "ownerId": {
                "305": "Automation user"
            },
            "companyEmployees": {},
            "companyBusinessType": {},
            "importedBy": {
                "305": "Automation user"
            },
            "pipeline": {},
            "createdBy": {
                "305": "Automation user"
   

```json
{
    "contact": {
        "mode": "CREATE",
        "details": {
            "firstName": "1662338177160",
            "lastName": "lasname_87",
            "emails": [
                {
                    "type": "OFFICE",
                    "value": "email@gmail.com",
                    "primary": true
                }
            ],
            "phoneNumbers": [
                {
                    "type": "MOBILE",
                    "code": "IN",
                    "dialCode": "+91",
                    "value": "8080808080",
                    "primary": true
                }
            ],
            "timezone": null
        }
    }
}
```

#### Convert Lead to Company
`POST https://api.kylas.io/v1/leads/{{lead_id}}/convert`

Convert lead into company using this API
Sample request payload
{
    "company": {
        "mode": "CREATE",
        "details": {
            "annualRevenue": {
                "currencyId": 431
            },
            "name": "Lead convert to New Company"
        }
    }
}
Sample response
{
    "ownerId": 305,
    "convertedAt": "2022-09-05T08:50:26.869+0000",
    "convertedBy": 305,
    "metaData": {
        "idNameStore": {
            "country": {},
            "convertedBy": {
                "305": "Automation user"
            },
            "updatedBy": {
                "305": "Automation user"
            },
            "timezone": {},
            "requirementCurrency": {},
            "source": {},
            "ownerId": {
                "305": "Automation user"
            },
            "companyEmployees": {},
            "companyBusinessType": {},
            "importedBy": {
                "305": "Automation user"
            },
            "pipeline": {},
            "createdBy": {
                "305": "Automation user"
            },
            "companyCountry": {},
            "campaign": {},
            "salutation": {},
            "pipelineStage": {},
            "cfCustomPiclist": {},
            "companyIndustry": {}
        }
    },
    "conversionDetails": [
        {
            "entityType": "COMPANY",
            "entityId": 11836
        }
    ]
}

```json
{
    "company": {
        "mode": "CREATE",
        "details": {
            "annualRevenue": {
                "currencyId": 431
            },
            "name": "Lead convert to New Company"
        }
    }
}
```

#### Send Email to Lead
`POST https://api.kylas.io/v1/emails`

Send email to lead using this API
Ensure Kylas user email is connected from Email settings here
To send email to many, add emailids in below object
{
    "id": null,
    "name": "extra@gmail.com",
    "entity": "email",
    "email": "extra@gmail.com"
}
Sample payload
{
    "subject": "sample email to lead",
    "": "",
    "body": "&lt;div&gt;this is sample email body&lt;/div&gt;&lt;div&gt;--&lt;/div&gt;&lt;div&gt;&amp;nbsp;&lt;/div&gt;",
    "relatedTo": {
        "id": 297575,
        "entity": "lead",
        "name": "lead 1662338519860",
        "email": "lead_1662338519860@mailinator.com"
    },
    "to": [
        {
            "id": "297575",
            "name": "lead 1662338519860",
            "entity": "lead",
            "email": "lead_1662338519860@mailinator.com"
        }
    ],
    "cc": [],
    "bcc": []
}
Sample response
{
    "id": 90158
}

```json
{
    "subject": "sample email to lead",
    "": "",
    "body": "<div>this is sample email body</div><div>--</div><div>&nbsp;</div>",
    "relatedTo": {
        "id": 297575,
        "entity": "lead",
        "name": "Vijay verma",
        "email": "vijay@mailinator.com"
    },
    "to": [
        {
            "id": 297575,
            "entity": "lead",
            "name": "Vijay verma",
            "email": "vijay@mailinator.com"
        }
    ],
    "cc": [],
    "bcc": []
}
```

#### Create Notes on Lead
`POST https://api.kylas.io/v1/notes/relation`

Create note on lead using this API
API KEY can be found here
Sample payload
{
    "sourceEntity": {
        "description": "lead is interested in product. Want to know more about it."
    },
    "targetEntityId": 79415,
    "targetEntityType": "LEAD"
}
Sample response
{
    "createdAt": "2022-09-05T09:08:52.326+0000",
    "updatedAt": "2022-09-05T09:08:52.326+0000",
    "createdBy": 305,
    "updatedBy": 305,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": false,
        "call": false,
        "sms": false,
        "task": false,
        "note": false,
        "meeting": false,
        "deleteAll": true,
        "quotation": false
    },
    "metaData": null,
    "id": 12639,
    "ownerId": 305,
    "tenantId": 173,
    "title": null,
    "description": "lead is interested in product. Want to know more about it.",
    "relation": null
}

```json
{
	"sourceEntity": {
		"description": "lead is interested in product. Want to know more about it."
	},
	"targetEntityId": {{lead_id}},
	"targetEntityType": "LEAD"
}
```

#### Delete Notes on Lead
`DELETE https://api.kylas.io/v1/notes/{{noteid}}`

#### Create Task on Lead
`POST https://api.kylas.io/v1/tasks/`

Create task on lead using this API

```json
{
    "type": 55084,
    "status": 55088,
    "reminder": "ONE_HOUR",
    "assignedTo": 4721,
    "relation": [
        {
            "targetEntityId": {{lead_id}},
            "targetEntityType": "LEAD"
        }
    ],
    "dueDate": "2021-10-30T11:00:00.000Z",
    "name": "task on lead",
    "customFieldValues": {}
}
```

#### Delete Task on Lead
`DELETE https://api.kylas.io/v1/tasks/{{task_id}}`

#### Create Meeting on Lead
`POST https://api.kylas.io/v1/meetings`

Create meeting on lead using this API
Add contacts, users or leads as participants by adding respective objects as below
{
            "id": "113020",            
            "entity": "contact"
        }
Sample request
{
    "title": "new meeting",
    "allDay": false,
    "timezone": {
        "id": 372,
        "name": "Asia/Calcutta"
    },
    "relatedTo": [
        {
            "id": "407236",            
            "entity": "lead"
        }
    ],
    "participants": [
        {
            "id": "407236",
            "entity": "lead"          
        }
    ],
    "from": "2022-10-18T17:00:00.000Z",
    "to": "2022-10-18T17:30:00.000Z"
}

```json
{
    "title": "new meeting",
    "allDay": false,
    "timezone": {
        "id": 372,
        "name": "Asia/Calcutta"
    },
    "relatedTo": [
        {
            "id": "407236",            
            "entity": "lead"
        }
    ],
    "participants": [
        {
            "id": "407236",
            "entity": "lead"          
        }
    ],
    "from": "2022-10-18T17:00:00.000Z",
    "to": "2022-10-18T17:30:00.000Z"
}
```

#### Get Lead Smartlist Filters
`GET https://api.kylas.io/v1/search-lists/lead?size=100`

#### Delete Lead
`DELETE https://api.kylas.io/v1/leads/{{lead_id}}`

#### Fetch Standard Picklist field values
`GET https://api.kylas.io/v1/fields/<field_id>`

Fetch picklist field values using this API.
Fetch any of lead/deal/contact/company field values. 
Lead fields page
Field id can be fetched from field details page
Sample response
{
    "field": {
        "createdAt": "2022-09-10T08:37:42.028+0000",
        "updatedAt": "2022-09-10T08:37:42.873+0000",
        "createdBy": 16955,
        "updatedBy": 16955,
        "id": 558644,
        "deleted": false,
        "version": 1,
        "recordActions": {
            "read": true,
            "write": false,
            "update": true,
            "delete": false,
            "email": false,
            "call": false,
            "sms": false,
            "task": false,
            "note": false,
            "meeting": false,
            "document": false,
            "readAll": true,
            "updateAll": true,
            "deleteAll": false,
            "quotation": false
        },
        "metaData": {
            "idNameStore": {}
        },
        "tenantId": 5543,
        "displayName": "Country",
        "description": null,
        "type": "PICK_LIST",
        "internalType": null,
        "name": "country",
        "entityType": null,
        "standard": true,
        "sortable": true,
        "filterable": true,
        "required": false,
        "important": false,
        "active": true,
        "multiValue": null,
        "length": null,
        "isUnique": null,
        "greaterThan": null,
        "lessThan": null,
        "lookupForEntity": null,
        "inte

#### Create Custom Text field
`POST https://api.kylas.io/v1/entities/lead/fields?entityType=lead`

Create custom text field on lead
{
    "displayName": "", // Enter text field name
    "description": "enter the text value",
    "pickLists": null,
    "filterable": true, // Mark false to make non-filterable
    "sortable": true, // Mark false to make non-sortable
    "standard": false,
    "required": false,
    "type": "TEXT_FIELD",
    "important": false
}

```json
{
    "displayName": "<custom text field name>",
    "description": "enter the text value",
    "pickLists": null,
    "filterable": true,
    "sortable": true,
    "standard": false,
    "required": false,
    "type": "TEXT_FIELD",
    "important": false
}
```

## Deal APIs

#### Create deal
`POST https://api.kylas.io/v1/deals/`

```json
{
    "ownedBy": {
        "id": {{Enter USer ID}},
        "name": "{{Enter User Name}}"
    },
    "name": "{{Enter Deal Name}}",
    "estimatedClosureOn": "2025-01-30T18:30:00.000Z",
    "estimatedValue": {
        "currencyId": 431,
        "value": 300
    },
    "pipeline": {
        "id": 15713,
        "name": "Default Deal Pipeline",
        "stage": {
            "id": 108606,
            "name": "Proposal Sent"
        }
    },
    "associatedContacts": [
        {
            "id": {{Enter Associated Contact Id}},
            "name": "Ethan Beard"
        }
    ],
    "company": {
        "id": {{Enter Associated Company Id}},
        "name": "Yundt, Schuppe and Welch"
    },
    "campaign": {
        "id": 52857,
        "name": "Organic",
        "disabled": false
    },
    "source": {
        "id": 52859,
        "name": "Facebook",
        "disabled": false
    },
    "products": [
        {
            "id": {{ENter Product ID}},
            "discount": {
                "value": 0,
                "type": "PERCENTAGE"
            },
            "name": "{{Prodcut Name}}",
            "quantity": 1,
            "units": null,
            "price": {
                "currencyId": 431,
                "value": 100
            },
            "overrideProductProperty": false
            // Setting this property to 'false' ensures that the product's  information is applied automatically, 
            // without needing to explicitly include it in the body data.
        }
    ],
    "subSource": "{{Enter subSource}}",
    "utmSource": "{{utmSource}}",
    "utmCampaign": "{{utmCampaign}}",
    "utmMedium": "{{utmMedium}}",
    "utmContent": "{{utmContent}}",
    "utmTerm": "{{utmTerm}}",
    "customFieldValues": {
        "cfTextField": "Sed autem id soluta ",
        "cfNumber": 367,
        "cfCheckbox": true,
        "cfUrlField": "https://app.kylas.io/sales/home",
        "cfParagraphText": "Qui architecto alias",
        "cfPickList": {
            "id": 54016,
            "name": "Monday"
        },
        "cfMultiPickList": [
            {
                "id": 54023,
                "name": "1"
            },
            {
                "id": 54024,
                "name": "2"
            },
            {
                "id": 54025,
                "name": "3"
            }
        ]
    }
}
```

#### Edit Deal
`PUT https://api.kylas.io/v1/deals/1804663`

```json
{
    "id": {{ENter Product ID}},
    "name": "{{Prodcut Name}}",
    "estimatedValue": {
        "value": 124312,
        "currencyId": 431
    },
    "actualValue": {
        "value": 124312,
        "currencyId": 431
    },
    "estimatedClosureOn": "2025-01-30T18:30:00.000Z",
    "pipeline": {
        "id": 15713,
        "name": "Default Deal Pipeline",
        "stage": {
            "id": 108606,
            "name": "Proposal Sent"
        }
    },
    "pipelineStageReason": null,
    "forecastingType": "OPEN",
    "associatedContacts": [
        {
            "id": 2611843,
            "name": "Ethan Beard"
        }
    ],
    "products": [
        {
            "id": {{ENter Product ID}},
            "name": "{{Prodcut Name}}",
            "quantity": 1,
            "price": {
                "currencyId": 431,
                "value": 100
            },
            "discount": {
                "type": "PERCENTAGE",
                "value": 0
            },
            "overrideProductProperty": false
             // Setting this property to 'false' ensures that the product's  information is applied automatically, 
        },
        {
            "id": {{ENter Product ID}},
            "discount": {
                "value": 0,
                "type": "PERCENTAGE"
            },
            "name": "{{Prodcut Name}}",
            "quantity": 1,
            "units": null,
            "price": {
                "currencyId": 431,
                "value": 124212
            },
            "category": {
                "id": 13311,
                "name": "Products"
            },
            "hsnSacCode": "74365214",
            "countryOfOrigin": {
                "id": 175,
                "name": "India"
            },
            "customFieldValues": {
                "cfPickList": {
                    "id": 17251,
                    "name": "Tuesday"
                }
            },
            "overrideProductProperty": true
            // This property is set to 'true' to ensure the product's information is added as per the product payload specifications.
        }
    ],
    "company": {
        "id": 825601,
        "name": "Yundt, Schuppe and Welch"
    },
    "ownedBy": {
        "id": 31706,
        "name": "Prod Sanity"
    },
    "createdBy": {
        "id": 31706,
        "name": "Prod Sanity"
    },
    "updatedBy": {
        "id": 31706,
        "name": "Prod Sanity"
    },
    "createdAt": "2025-01-02T11:32:47.474Z",
    "updatedAt": "2025-01-02T11:32:47.474Z",
    "actualClosureDate": null,
    "source": {
        "id": 52859,
        "name": "Facebook"
    },
    "campaign": {
        "id": 52857,
        "name": "Organic"
    },
    "customFieldValues": {
        "cfNumber": 367,
        "cfUrlField": "https://app.kylas.io/sales/home",
        "cfTextField": "Sed autem id soluta",
        "cfCheckbox": true,
        "cfParagraphText": "Qui architecto alias",
        "cfPickList": {
            "id": 54016,
            "name": "Monday"
        },
        "cfMultiPickList": [
            {
                "id": 54023,
                "name": "1"
            },
            {
                "id": 54024,
                "name": "2"
            },
            {
                "id": 54025,
                "name": "3"
            }
        ]
    },
    "isNew": true,
    "latestActivityCreatedAt": null,
    "meetingScheduledOn": null,
    "taskDueOn": null,
    "createdViaId": "31706",
    "createdViaName": "User",
    "createdViaType": "Web",
    "updatedViaId": null,
    "updatedViaName": null,
    "updatedViaType": null,
    "subSource": "{{Enter subSource}}",
    "utmSource": "{{utmSource}}",
    "utmCampaign": "{{utmCampaign}}",
    "utmMedium": "{{utmMedium}}",
    "utmContent": "{{utmContent}}",
    "utmTerm": "{{utmTerm}}",
    "importedBy": null,
    "estimatedValueExchangeRate": {
        "431": 1
    },
    "estimatedValueExchangeDate": "2025-01-02T11:32:47.384Z",
    "actualValueExchangeRate": {
        "431": 1
    },
    "actualValueExchangeDate": "2025-01-02T11:32:47.384Z"
}
```

#### Get Deal details
`GET https://api.kylas.io/v1/deals/<deal_id>`

Fetch deal details using this API
Sample response:
{
    "id": 59217,
    "name": "sample deal",
    "estimatedValue": {
        "currencyId": 400,
        "value": 24000.0
    },
    "actualValue": {
        "currencyId": 400,
        "value": 21600.0
    },
    "estimatedClosureOn": "2022-09-14T06:30:00Z",
    "pipeline": {
        "id": 2,
        "name": "Default Deal Pipeline",
        "stage": {
            "id": 5,
            "name": "Open"
        }
    },
    "pipelineStageReason": null,
    "forecastingType": "OPEN",
    "associatedContacts": [{
        "id": 17,
        "name": "vishnu sarma"
    }],
    "products": [{
        "id": 26408,
        "name": "TATA SKY TSK (V) -43-DTH-TATA",
        "quantity": 12,
        "price": {
            "currencyId": 400,
            "value": 2000.0
        },
        "discount": {
            "type": "PERCENTAGE",
            "value": 10.0
        }
    }],
    "company": {
        "id": 25784,
        "name": "Tata Projects"
    },
    "ownedBy": {
        "id": 2,
        "name": "Kiran N"
    },
    "createdBy": {
        "id": 1,
        "name": "Gaurav Pasaarkar"
    },
    "updatedBy": {
        "id": 1,
        "name": "Gaurav Pasaarkar"
    },
    "createdAt": "2022-09-13T13:10:20Z",
    "updatedAt": "2022-09-13T13:10:20Z",
    "actualClosureDate": null,
    "source": {
        "id": 4022,
        "name": "Google"
    },
    "campaign": {
        "id": 4021,
        "name": "Organic"
    },
    "customFieldValues": {

```json
{}
```

#### Update deal
`PATCH https://api.kylas.io/v1/deals/<enter_deal_id>`

```json
[
    //Deal name
    {
        "op": "replace",
        "path": "/name",
        "value": "Patch Test 1"
    },
    //Associated Contact
    {
        "op": "replace",
        "path": "/associatedContacts/0",
        "value": {
            "id": 260110,
            "name": "Margarett Von"
        }
    },
    //Pipeline
    {
        "op": "add",
        "path": "/pipeline",
        "value": {
            "id": 6134,
            "name": "Default Deal Pipeline ",
            "stage": {
                "id": 38476,
                "name": "Proposal Sent"
            }
        }
    },
    //Product
    {
        "op": "add",
        "path": "/products/0",
        "value": {
            "id": 23006,
            "discount": {
                "value": 0,
                "type": "PERCENTAGE"
            },
            "name": "2 Bhk Flat",
            "quantity": 1,
            "price": {
                "currencyId": 431,
                "value": 5
            },
            "category": {
                "id": 33828,
                "name": "Products"
            },
            "hsnSacCode": "40131010",
            "countryOfOrigin": {
                "id": 175,
                "name": "India"
            },
            "customFieldValues": {
                "cfDateTimePickerTest": "2023-05-10T06:00:00.000Z",
                "cfDateTest": "2023-11-30T06:30:00.000Z",
                "cfCheckbox": true,
                "cfNumberTest": 51,
                "cfTextFieldTest": "Text field test"
            }
        }
    },
    //Campaign Information
    {
        "op": "remove",
        "path": "/subSource",
        "value": "subSource"
    },
    {
        "op": "remove",
        "path": "/utmSource",
        "value": "utmSource"
    },
    {
        "op": "remove",
        "path": "/utmCampaign",
        "value": "utmCampaign"
    },
    {
        "op": "replace",
        "path": "/utmMedium",
        "value": "utmMedium"
    },
    {
        "op": "replace",
        "path": "/utmContent",
        "value": "utmContent"
    },
    {
        "op": "add",
        "path": "/utmTerm",
        "value": "utmTerm"
    },
    {
        "op": "add",
        "path": "/source",
        "value": {
            "id": 13326,
            "name": "Facebook"
        }
    },
    {
        "op": "add",
        "path": "/campaign",
        "value": {
            "id": 15495,
            "name": "Goverment"
        }
    },
    //Custom fields 
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiValuePicklistTest",
        "value": []
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiValuePicklistTest/0",
        "value": {
            "id": 13998,
            "name": "Monday"
        }
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfTextFieldTest",
        "value": "updated by patch"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfParagraphTextTest",
        "value": "Add paragraph  description"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfNumberTest",
        "value": 13
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfUrlFieldTest",
        "value": "https://app.kylas.io/"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfPickListTest",
        "value": {
            "id": 13401,
            "name": "Saturday"
        }
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfDateTest",
        "value": "2023-12-13T06:30:00.000Z"
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfCheckboxTest",
        "value": true
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfDateTimeTest",
        "value": "2023-12-13T11:30:00.000Z"
    },
    //Owner
    {
        "op": "replace",
        "path": "/ownedBy",
        "value": {
            "id": 8146,
            "name": "Rohit Sharma"
        }
    },
    //estimatedClosureOn
    {
        "op": "add",
        "path": "/estimatedClosureOn",
        "value": "2023-11-02T06:30:00.000Z"
    },
    //estimatedValue
    {
        "op": "add",
        "path": "/estimatedValue",
        "value": {
            "currencyId": 431,
            "value": 1000
        }
    },
    //actualValue
    {
        "op": "add",
        "path": "/actualValue",
        "value": {
            "currencyId": 431,
            "value": 1000
        }
    },
    //Company
    {
        "op": "add",
        "path": "/company",
        "value": {
            "id": 15627,
            "name": "Rau, Hirthe and Schuster"
        }
    }
]
```

#### Search Deal
`POST https://api.kylas.io/v1/search/deal?page=0&size=10&sort=updatedAt,desc`

Search deals using this API
Kylas deals can be searched by any of below keywords
1.Deal Stage
2.Deal Name
3.Company associated to deal
4.Contact associated to deal
Enter the value to be searched against the key in request body: "value": "search_keyword"
Sample response:
{
    "content": [{
        "pipeline": {
            "name": "Default Deal Pipeline",
            "id": 2
        },
        "estimatedValue": {
            "currencyId": 400,
            "value": 24000.0
        },
        "customFieldValues": {
            "text": "custom  text field"
        },
        "name": "sample deal",
        "actualClosureDate": null,
        "company": {
            "name": "Tata Projects",
            "id": 25784
        },
        "id": 59217,
        "ownerId": 2,
        "pipelineStage": {
            "name": "Open",
            "id": 5
        },
        "recordActions": {
            "read": true,
            "write": true,
            "update": true,
            "delete": true,
            "email": true,
            "call": true,
            "sms": true,
            "task": true,
            "note": true,
            "meeting": true,
            "readAll": true,
            "updateAll": true,
            "deleteAll": true,
            "quotation": true
        },
        "ownedBy": {
            "name": "Kiran N",
            "id": 2
        },
        "estimatedClosureOn": "2022-09-14T06:30:00.000Z"
    }, {
        "pipeline": null,
        "estimatedValue": {
           

```json
{
    "fields": [
        "name",
        "ownedBy",
        "estimatedValue",
        "estimatedClosureOn",
        "company",
        "pipeline",
        "pipelineStage",
        "actualClosureDate",
        "customFieldValues",
        "id"
    ],
    "jsonRule": {
        "condition": "AND",
        "rules": [
            {
                "id": "multi_field",
                "field": "multi_field",
                "type": "multi_field",
                "input": "multi_field",
                "operator": "multi_field",
                "value": "open"
            }
        ],
        "valid": true
    }
}
```

#### Change Deal Pipeline Stage
`POST https://api.kylas.io/v1/deals/<Enter_deal_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Change deal pipeline stage from any stage to any stage.
Fetch deal Pipeline and stage Ids from here
Product IDs can be fetched from here
Sample payload with products
{
    "reasonForClosing": null,
    "actualValue": {
        "currencyId": 400,
        "value": 4290
    },
    "products": [{
        "id": 16691,
        "discount": {
            "value": 0,
            "type": "PERCENTAGE"
        },
        "name": "003L30 - LAVA -01-WATER HEATER-VENUS",
        "quantity": 1,
        "price": {
            "currencyId": 431,
            "value": 4290
        }
    }]
}
Sample payload without products
{
    "reasonForClosing": null,
    "actualValue": {
        "currencyId": 400,
        "value": 200
    },
    "products": null
}

```json
{
    "reasonForClosing": null,
    "actualValue": {
        "currencyId": 400,
        "value": 200
    },
    "products": null
}
```

#### Mark Deal as WON
`POST https://api.kylas.io/v1/deals/<Enter_deal_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Change deal pipeline stage from any stage to any stage.
Fetch deal Pipeline and stage Ids from here
Product IDs can be fetched from here
Sample payload with products
{
    "reasonForClosing": null,
    "actualValue": {
        "currencyId": 400,
        "value": 4290
    },
    "products": [{
        "id": 16691,
        "discount": {
            "value": 0,
            "type": "PERCENTAGE"
        },
        "name": "003L30 - LAVA -01-WATER HEATER-VENUS",
        "quantity": 1,
        "price": {
            "currencyId": 431,
            "value": 4290
        }
    }]
}
Sample payload without products
{
    "reasonForClosing": null,
    "actualValue": {
        "currencyId": 400,
        "value": 200
    },
    "products": null
}
Sample response
{
    "id": 4393,
    "name": "new pipeline",
    "unqualifiedReasons": ["Budget does not match", "False enquiry", "Wrong number", "Customer already bought the product/service", "Bought product/service with competitor", "Did not pick phone", "Not interested anymore", "Duplicate Customer", "unqualified reason"],
    "lostReasons": ["No followup", "Not interested", "Booked with competitor", "Not answering/responding", "Bought product/service with competitor", "Low budget", "Postponed the decision of buying product/service", "lost reason"],
    "stages": [{
        "id": 27537,
        "name": "Open",
        "forecastingType": "OPEN",
        "description": "When a Deal is just created in the system and there is no activity initiated 

```json
{
    "reasonForClosing": null,
    "actualValue": {
        "currencyId": 400,
        "value": 200
    },
    "products": null
}
```

#### Mark Deal as Closed Lost
`POST https://api.kylas.io/v1/deals/<Enter_deal_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Change deal pipeline stage from any stage to Closed Lost.
Fetch deal Pipeline and stage Ids from here
Product IDs can be fetched from here
Sample response
{
    "id": 4393,
    "name": "new pipeline",
    "unqualifiedReasons": ["Budget does not match", "False enquiry", "Wrong number", "Customer already bought the product/service", "Bought product/service with competitor", "Did not pick phone", "Not interested anymore", "Duplicate Customer", "unqualified reason"],
    "lostReasons": ["No followup", "Not interested", "Booked with competitor", "Not answering/responding", "Bought product/service with competitor", "Low budget", "Postponed the decision of buying product/service", "lost reason"],
    "stages": [{
        "id": 27537,
        "name": "Open",
        "forecastingType": "OPEN",
        "description": "When a Deal is just created in the system and there is no activity initiated in order to proceed ahead with the Deal, it’s called Open Deal.",
        "position": 1,
        "status": "COMPLETED",
        "startedAt": "2022-09-23T08:01:25.737Z",
        "completedAt": "2022-09-23T08:01:33.25Z",
        "reason": null,
        "winLikelihood": 0
    }, {
        "id": 27538,
        "name": "Won",
        "forecastingType": "CLOSED_WON",
        "description": "When the sale of the product for which the Deal was created has been done successfully, a Deal is considered as Won Deal",
        "position": 2,
        "status": "SKIPPED",
        "startedAt": null,
        "comp

```json
{
    "reasonForClosing": "No followup",
    "actualValue": null
}
```

#### Mark Deal as Closed Unqualified
`POST https://api.kylas.io/v1/deals/<Enter_deal_id>/pipeline-stages/<Enter_pipeline_stage_id>/activate`

Change deal pipeline stage from any stage to Closed Unqualified.
Fetch deal Pipeline and stage Ids from here
Product IDs can be fetched from here
Sample response
{
    "id": 4393,
    "name": "new pipeline",
    "unqualifiedReasons": ["Budget does not match", "False enquiry", "Wrong number", "Customer already bought the product/service", "Bought product/service with competitor", "Did not pick phone", "Not interested anymore", "Duplicate Customer", "unqualified reason"],
    "lostReasons": ["No followup", "Not interested", "Booked with competitor", "Not answering/responding", "Bought product/service with competitor", "Low budget", "Postponed the decision of buying product/service", "lost reason"],
    "stages": [{
        "id": 27537,
        "name": "Open",
        "forecastingType": "OPEN",
        "description": "When a Deal is just created in the system and there is no activity initiated in order to proceed ahead with the Deal, it’s called Open Deal.",
        "position": 1,
        "status": "COMPLETED",
        "startedAt": "2022-09-23T08:03:10.377Z",
        "completedAt": "2022-09-23T08:03:19.763Z",
        "reason": null,
        "winLikelihood": 0
    }, {
        "id": 27538,
        "name": "Won",
        "forecastingType": "CLOSED_WON",
        "description": "When the sale of the product for which the Deal was created has been done successfully, a Deal is considered as Won Deal",
        "position": 2,
        "status": "SKIPPED",
        "startedAt": null,
     

```json
{
    "reasonForClosing": "Budget does not match",
    "actualValue": null
}
```

#### Create Call log on Deal
`POST https://api.kylas.io/v1/call-logs/`

Use this API to create call log on deal.
Duration is always in seconds
"duration": "300",

```json
{
    "relatedTo": {
        "id": 25693,
        "entity": "deal",
        "phoneNumber": "8080808080"
    },
    "associatedTo": [
        {
            "id": 113021,
            "entity": "contact",
            "phoneNumber": "8080808080"
        }
    ],
    "outcome": "connected",
    "startTime": "2022-09-05T10:53:44.430Z",
    "phoneNumber": "8080808080",
    "callType": "outgoing",
    "duration": "300",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "callRecording": {
        "data": "",
        "fileName": "sampel.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}
```

#### Delete Deal
`DELETE https://api.kylas.io/v1/deals/<deal_id>`

Delete Deal using this API

```json
{}
```

#### Create Notes on Deal
`POST https://api.kylas.io/v1/notes/relation`

Add note on deal using this API.

```json
{
    "sourceEntity": {
        "description": "<div>notes on deal</div>"
    },
    "targetEntityId": "35257",
    "targetEntityType": "DEAL"
}
```

#### Create Task on Deal
`POST https://api.kylas.io/v1/tasks/`

Create task on deal using this API
IDs for task type, status and priority options can be fetched from Task Layout API under Tasks API folder
Sample response:
{
    "createdAt": "2022-09-13T13:23:56.616+0000",
    "updatedAt": "2022-09-13T13:23:56.616+0000",
    "createdBy": 1,
    "updatedBy": 1,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": false,
        "call": false,
        "sms": false,
        "task": false,
        "note": true,
        "meeting": false,
        "document": false,
        "deleteAll": true,
        "quotation": false
    },
    "metaData": {
        "idNameStore": {
            "updatedBy": {
                "1": "Gaurav Pasaarkar"
            },
            "createdBy": {
                "1": "Gaurav Pasaarkar"
            },
            "ownerId": {
                "1": "Gaurav Pasaarkar"
            },
            "type": {
                "706": "Call"
            },
            "priority": {
                "713": "High"
            },
            "assignedTo": {
                "2": "Kiran N"
            },
            "status": {
                "710": "Open"
            },
            "relation": {}
        }
    },
    "id": 414084,
    "ownerId": 1,
    "tenantId": 1,
    "name": "sample task on deal",
    "description": null,
    "type": 706,
    "dueDate": "2022-09-13T13:30:00.000+0000",
    "reminder": "ONE_HOUR",
    "status": 710,
    "priority": 713,
    "assignedTo": 2,
 

```json
{
	"reminder": "ONE_HOUR",
	"assignedTo": 2,
	"relation": [{
		"targetEntityId": "59217",
		"targetEntityType": "DEAL"
	}],
	"dueDate": "2022-09-13T13:30:00.000Z",
	"name": "sample task on deal",
	"type": 706,
	"status": 710,
	"priority": 713,
	"customFieldValues": {}
}
```

#### Create Meeting on Deal
`POST https://api.kylas.io/v1/meetings`

```json
{
    "title": "meeting on deal",
    "description": "sample desc",
    "allDay": false,
    "timezone": {
        "id": 372,
        "name": "Asia/Calcutta"
    },
    "location": "mumbai",
    "medium": "OFFLINE",
    "status": "scheduled",
    "relatedTo": [
        {
            "id": "35257",
            "name": "s-Credit Card Account",
            "entity": "deal"
        },
        {
            "id": 2264185,
            "entity": "lead"
        }
    ],
    "participants": [
        {
            "id": 2264185,
            "entity": "lead",
            "name": "new test lead",
            "email": null
        }
    ],
    "from": "2023-09-05T11:30:00.000Z",
    "to": "2023-09-05T12:00:00.000Z"
}
```

#### Add Quotation on deal
`POST https://api.kylas.io/v1/quotations/`

Use this API to add quotation on deal
Product ids and details available here

```json
{
    "currencyId": 400,
    "additionalDiscount": {
        "type": "PERCENTAGE",
        "value": 0
    },
    "additionalTax": 0,
    "adjustment": {
        "type": "PERCENTAGE",
        "value": 0
    },
    "isBillingAndShippingAddressSame": true,
    "status": {
        "id": "DRAFT",
        "name": "Draft"
    },
    "subTotal": 4290,
    "grandTotal": 4290,
    "owner": {
        "id": 1,
        "name": "Gaurav Pasaarkar"
    },
    "summary": "s-Credit Card Account",
    "associatedDeal": {
        "id": "35257",
        "name": "s-Credit Card Account"
    },
    "associatedContacts": [
        {
            "id": 49724,
            "name": "a 1080p"
        }
    ],
    "associatedCompany": {
        "id": 30377,
        "name": "lead to company"
    },
    "products": [
        {
            "id": 16691,
            "tax": 0,
            "discount": {
                "value": 0,
                "type": "PERCENTAGE"
            },
            "name": "003L30 - LAVA -01-WATER HEATER-VENUS",
            "quantity": 1,
            "price": {
                "currencyId": 431,
                "value": 4290
            },
            "description": null,
            "totalAmount": {
                "currencyId": 431,
                "value": 4290
            }
        }
    ],
    "quotationNumber": "123456",
    "generationDate": "2022-09-06T11:40:54.273Z",
    "validTill": "2022-09-23T18:29:59.999Z",
    "billingAddress": "billing address",
    "shippingAddress": "billing address",
    "billingCity": "billing city",
    "shippingCity": "billing city",
    "billingState": "billing state",
    "shippingState": "billing state",
    "billingCountry": {
        "id": 175,
        "name": "India",
        "disabled": false
    },
    "shippingCountry": {
        "id": 175,
        "name": "India",
        "disabled": false
    },
    "billingPinCode": "411033",
    "shippingPinCode": "411033",
    "additionalInformation": "<div>additional information about quote</div>",
    "customFieldValues": {}
}
```

#### Create Deal webhook
`POST https://api.kylas.io/v1/webhooks`

Create Deal webhook for deal create, update and delete.

```json
{
    "name": "deal webhook for create update and delete ",
    "requestType": "POST",
    "url": "https://www.<enter_webhook_url>",
    "authenticationType": "NONE",
    "authenticationKey": null,
    "events": [
        "DEAL_UPDATED",
        "DEAL_CREATED",
        "DEAL_DELETED"
    ],
    "active": true
}
```

#### Upload document on deal
`POST https://api.kylas.io/v1/documents`

Upload document on deal using this API.
Under 'Select Files' section of the body, choose the file using the file system which you want to upload on deal.
Sample response:
{
    "success": [
        {
            "id": 6038,
            "fileName": "Screenshot from 2023-01-09 15-28-33.png"
        }
    ],
    "failure": []
}

## Contact APIs

#### Create Contact
`POST https://api.kylas.io/v1/contacts`

Create Contact API creates contact with  required values as below. Review below snippet and set values are per your requirement, Whichever value is not required, set null
API KEY can be found here
Custom field values should be placed in customFieldValues object as below
"customFieldValues": {
        "cfcompany":"this is custom field"
    }
Company id can be fetched from company details page url
Below is the sample request payload
{
    "firstName": "fname",
    "lastName": "lname",
    "emails": [
        {
            "type": "OFFICE",
            "value": "prd@mailinator.com",
            "primary": true
        }
    ],
    "address": "address",
    "city": "city",
    "state": "state",
    "zipcode": "510089",
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "dialCode": "+91",
            "value": "9090909090",
            "primary": true
        }
    ],
    "department": "dadas",
    "designation": "adasdsaas",
    "country": "IN",
    "facebook": null,
    "twitter": null,
    "linkedin": null,
    "customFieldValues": {
        "cfcompany":"this is custom field"
    }
}
Below is the sample response
{
    "createdAt": "2022-09-06T06:26:53.583+0000",
    "updatedAt": "2022-09-06T06:26:53.583+0000",
    "createdBy": 305,
    "updatedBy": 305,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": true,
        "call": true,
        "sms": true,
        "task": true,

```json
{
    "firstName": "fname",
    "lastName": "lname",
    "emails": [
        {
            "type": "OFFICE",
            "value": "prd@mailinator.com",
            "primary": true
        }
    ],
    "address": "address",
    "city": "city",
    "state": "state",
    "zipcode": "510089",
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "dialCode": "+91",
            "value": "9090909090",
            "primary": true
        }
    ],
    "department": "dadas",
    "designation": "adasdsaas",
    "country": "IN",
    "facebook": null,
    "twitter": null,
    "linkedin": null,
    "customFieldValues": {
        "cfcompany":"this is custom field"
    }
}
```

#### Search Contact API
`POST https://api.kylas.io/v1/search/contact?sort=updatedAt,desc&page=0&size=10`

Search API searches for a Contact based on the search key value. Search key value can be any of below:

Contact Name (both first name and last name)
Contact Phone number
Contact Email
Contact Company Name
Contact Department
Contact Designation

Replace the keyword against "value" key   with the desired search keyword in below JSON
{"fields":["firstName","lastName","ownerId","company","designation","id","recordActions","customFieldValues"],"jsonRule":{"rules":[{"id":"multi_field","field":"multi_field","type":"multi_field","input":"multi_field","operator":"multi_field","value":"vishnu"}],"condition":"AND","valid":true}}

```json
{
    "fields": [
        "firstName",
        "lastName",
        "ownerId",
        "company",
        "designation",
        "id",
        "recordActions",
        "customFieldValues"
    ],
    "jsonRule": {
        "rules": [
            {
                "id": "multi_field",
                "field": "multi_field",
                "type": "multi_field",
                "input": "multi_field",
                "operator": "multi_field",
                "value": "vishnu"
            }
        ],
        "condition": "AND",
        "valid": true
    }
}
```

#### Get  Contact details
`GET https://api.kylas.io/v1/contacts/<contact_id>`

Fetch contact details using this API
Sample response
{
    "createdAt": "2020-07-28T06:24:27.413+0000",
    "updatedAt": "2020-07-28T06:24:27.413+0000",
    "createdBy": 5,
    "updatedBy": 5,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": true,
        "call": true,
        "sms": true,
        "task": true,
        "note": true,
        "meeting": true,
        "document": true,
        "deleteAll": true,
        "quotation": true
    },
    "metaData": {
        "idNameStore": {
            "country": {},
            "updatedBy": {
                "5": "Kireeti A"
            },
            "test": {},
            "createdBy": {
                "5": "Kireeti A"
            },
            "dumyPicklist": {},
            "timezone": {},
            "company": {},
            "salutation": {},
            "ownerId": {
                "5": "Kireeti A"
            }
        }
    },
    "id": 17,
    "ownerId": 5,
    "firstName": "vishnu",
    "lastName": "sarma",
    "dnd": false,
    "timezone": "Asia/Calcutta",
    "stakeholder": false
}

#### Update Contact
`PUT https://api.kylas.io/v1/contacts/<contact_id>`

Update Contact currently is a PUT request and It is a 3 step process for now

Fetch contact details using 'Get contact details' API.
From above request's response, update those fields which you want.
Copy paste the new payload in Update company request's body and hit 'Send' request.

API KEY can be found here
Company ID can be found in company details page url.
Find Ids as below:

For any form field details like picklist value ids, Company type ids, Campaign, Source, any Custom fields and their value ids visit here

```json
{
  "salutation": 1751,
  "firstName": "Testing contact",
  "lastName": "API",
  "phoneNumbers": [
    {
      "type": "MOBILE",
      "code": "IN",
      "value": "09877878767",
      "dialCode": "+91",
      "primary": true
    }
  ],
  "emails": [
    {
      "type": "OFFICE",
      "value": "kylastesing25@gmail.com",
      "primary": true
    }
  ],
  "customFieldValues": {
    "testingCustom": true
  },
  "dnd": true,
  "timezone": "Pacific/Midway",
  "address": "Alphanta Spicexss",
  "city": "Mumbai",
  "state": "Maharashtra",
  "zipcode": "400605",
  "country": "AS",
  "facebook": "https://fb.com",
  "twitter": "https://fb.com",
  "linkedin": "https://fb.com",
  "company": 894,
  "department": "qedcewcf",
  "designation": "asdcwsc",
  "stakeholder": true
}
```

#### Get all Contacts form fields
`GET https://api.kylas.io/v1/entities/contact/fields?entityType=contact&custom-only=false&sort=createdAt,asc&page=0&size=10`

Fetch contact form fields and their details using this API
Sample response
[
    {
        "createdAt": "2021-09-30T10:02:17.834+0000",
        "updatedAt": "2021-09-30T10:02:19.620+0000",
        "createdBy": 4721,
        "updatedBy": 4721,
        "id": 194341,
        "deleted": false,
        "version": 1,
        "recordActions": null,
        "metaData": null,
        "tenantId": 2240,
        "displayName": "Salutation",
        "description": null,
        "type": "PICK_LIST",
        "internalType": null,
        "name": "salutation",
        "entityType": null,
        "standard": true,
        "sortable": true,
        "filterable": true,
        "required": false,
        "important": false,
        "active": true,
        "multiValue": null,
        "length": null,
        "isUnique": null,
        "greaterThan": null,
        "lessThan": null,
        "lookupForEntity": null,
        "internal": false,
        "lookupUrl": null,
        "skipIdNameResolution": false,
        "picklist": {
            "createdAt": "2021-09-30T10:02:17.835+0000",
            "updatedAt": "2021-09-30T10:02:17.835+0000",
            "createdBy": 4721,
            "updatedBy": 4721,
            "id": 14222,
            "deleted": false,
            "version": 0,
            "recordActions": null,
            "metaData": null,
            "tenantId": 2240,
            "name": "",
            "displayName": null,
            "global": false,
            "systemDefault": false,
       

#### Delete Contact
`DELETE https://api.kylas.io/v1/contacts/<contact_id>`

Delete Contact using this API

#### Create Note on Contact
`POST https://api.kylas.io/v1/notes/relation`

Use this API to create note on contact
Sample payload below
{
    "sourceEntity": {
        "description": "&lt;div&gt;note on contact&lt;/div&gt;"
    },
    "targetEntityId": "17",
    "targetEntityType": "CONTACT"
}
Sample response below
{
    "createdAt": "2022-09-06T07:15:35.966+0000",
    "updatedAt": "2022-09-06T07:15:35.966+0000",
    "createdBy": 1,
    "updatedBy": 1,
    "recordActions": {
        "read": true,
        "update": true,
        "delete": true,
        "email": false,
        "call": false,
        "sms": false,
        "task": false,
        "note": false,
        "meeting": false,
        "document": false,
        "deleteAll": true,
        "quotation": false
    },
    "metaData": null,
    "id": 1404364,
    "ownerId": 1,
    "tenantId": 1,
    "title": null,
    "description": "&lt;div&gt;note on contact&lt;/div&gt;",
    "relation": null
}

```json
{
    "sourceEntity": {
        "description": "<div>note on contact</div>"
    },
    "targetEntityId": "17",
    "targetEntityType": "CONTACT"
}
```

#### Create Task on Contact
`POST https://api.kylas.io/v1/tasks/`

Create task on contact using this API
Sample payload below
{
    "reminder": "ONE_HOUR",
    "assignedTo": 1,
    "relation": [
        {
            "targetEntityId": "17",
            "targetEntityType": "CONTACT"
        }
    ],
    "dueDate": "2022-09-06T07:30:00.000Z",
    "name": "task on contact",
    "type": 707,
    "status": 710,
    "priority": 713,
    "customFieldValues": {}
}

```json
{
    "reminder": "ONE_HOUR",
    "assignedTo": 1,
    "relation": [
        {
            "targetEntityId": "17",
            "targetEntityType": "CONTACT"
        }
    ],
    "dueDate": "2022-09-06T07:30:00.000Z",
    "name": "task on contact",
    "type": 707,
    "status": 710,
    "priority": 713,
    "customFieldValues": {}
}
```

#### Create Call log on Contact
`POST https://api.kylas.io/v1/call-logs/`

Add call log on contact using this API.
Sample request payload below
{
    "outcome": "connected",
    "startTime": "2022-09-02T08:05:44.370Z",
    "phoneNumber": "9848022338",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "entity": "contact",
        "id": 112936,
        "phoneNumber": "9848022338"
    },
    "callRecording": {
        "data": "",
        "fileName": "sampel.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}

```json
{
    "outcome": "connected",
    "startTime": "2022-09-02T08:05:44.370Z",
    "phoneNumber": "9848022338",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "entity": "contact",
        "id": 112936,
        "phoneNumber": "9848022338"
    },
    "callRecording": {
        "data": "",
        "fileName": "sampel.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}
```

#### Create Meeting on Contact
`POST https://api.kylas.io/v1/meetings`

Create meeting on contact using this API
Add participants by adding their details in below object
"participants": [
        {
            "id": "17",
            "entity": "user",
            "name": "test user",
            "email": "dave@mailinator.com"
        }
    ],
Sample request payload
{
    "title": "meeting on contact",
    "description": "sample desc",
    "allDay": false,
    "timezone": {
        "id": 372,
        "name": "Asia/Calcutta"
    },
    "location": "mumbai",
    "medium": "OFFLINE",
    "status": "scheduled",
    "relatedTo": [
        {
            "id": "17",
            "name": "vishnu sarma",
            "entity": "contact"
        },
        {
            "id": 30377,
            "name": "lead to company",
            "entity": "company"
        }
    ],
    "participants": [
        {
            "id": "17",
            "entity": "contact",
            "name": "vishnu sarma",
            "email": null
        }
    ],
    "from": "2022-09-06T07:30:00.000Z",
    "to": "2022-09-06T08:00:00.000Z"
}

```json
{
    "title": "meeting on contact",
    "description": "sample desc",
    "allDay": false,
    "timezone": {
        "id": 372,
        "name": "Asia/Calcutta"
    },
    "location": "mumbai",
    "medium": "OFFLINE",
    "status": "scheduled",
    "relatedTo": [
        {
            "id": "17",
            "name": "vishnu sarma",
            "entity": "contact"
        },
        {
            "id": 30377,
            "name": "lead to company",
            "entity": "company"
        }
    ],
    "participants": [
        {
            "id": "17",
            "entity": "contact",
            "name": "vishnu sarma",
            "email": null
        }
    ],
    "from": "2022-09-06T07:30:00.000Z",
    "to": "2022-09-06T08:00:00.000Z"
}
```

#### Send Email to Contact
`POST https://api.kylas.io/v1/emails`

Send email to contact using this API
Ensure Kylas user email is connected from Email settings here
To send email to many, add emailids in below object
 "to": [{
    "id": null,
    "name": "extra@gmail.com",
    "entity": "email",
    "email": "extra@gmail.com"
}]
Sample request payload
{
    "subject": "sample email to lead",
    "": "",
    "body": "&lt;div&gt;this is sample email body&lt;/div&gt;&lt;div&gt;--&lt;/div&gt;&lt;div&gt;&amp;nbsp;&lt;/div&gt;",
    "relatedTo": {
        "id": 297575,
        "entity": "contact",
        "name": "Vijay verma",
        "email": "vijay@mailinator.com"
    },
    "to": [
        {
            "id": 297575,
            "entity": "contact",
            "name": "Vijay verma",
            "email": "vijay@mailinator.com"
        }
    ],
    "cc": [],
    "bcc": []
}

```json
{
    "subject": "sample email to lead",
    "": "",
    "body": "<div>this is sample email body</div><div>--</div><div>&nbsp;</div>",
    "relatedTo": {
        "id": 297575,
        "entity": "contact",
        "name": "Vijay verma",
        "email": "vijay@mailinator.com"
    },
    "to": [
        {
            "id": 297575,
            "entity": "contact",
            "name": "Vijay verma",
            "email": "vijay@mailinator.com"
        }
    ],
    "cc": [],
    "bcc": []
}
```

#### Update Contact Patch
`PATCH https://api.kylas.io/v1/contacts/{{Contact_ID}}`

```json
[
    // Note: Replace operation can only be performed if the field already exists. 
// If the field is empty or not initialized, use "add" operation instead.
    // -------------------------------
    // 1. Basic Information
    // -------------------------------
    {
        "op": "add",
        "path": "/ownerId",
        "value": 11622
    }, // Owner of the contact
    {
        "op": "remove",
        "path": "/salutation",
        "value": 479484
    }, // Salutation of contact (Mr., Ms., Miss., etc.)
    {
        "op": "replace",
        "path": "/firstName",
        "value": "First name Patch"
    }, // First name of the contact
    {
        "op": "replace",
        "path": "/lastName",
        "value": "last Name Patch"
    }, // Last name of the contact

    // -------------------------------
    // 2. Communication Information
    // -------------------------------
    {
        "op": "replace",
        "path": "/emails/0",
        "value": {
            "type": "OFFICE",
            "value": "user1patch@flexvio.com",
            "primary": true
        }
    },  // Primary office email
    {
        "op": "replace",
        "path": "/emails/1",
        "value": {
            "type": "OFFICE",
            "value": "patchuser@flexvio.com",
            "primary": false
        }
    },// Secondary office email
    {
        "op": "replace",
        "path": "/phoneNumbers/0",
        "value": {
            "id": null,
            "type": "MOBILE",
            "code": "IN",
            "value": "8734523499",
            "dialCode": "+91",
            "primary": true
        }
    }, // Primary mobile number
    {
        "op": "replace",
        "path": "/phoneNumbers/1",
        "value": {
            "id": null,
            "type": "MOBILE",
            "code": "IN",
            "value": "8734523487",
            "dialCode": "+91",
            "primary": false
        }
    }, // Secondary mobile number
    {
        "op": "add",
        "path": "/dnd",
        "value": true
    }, // Do Not Disturb flag for contact
    {
        "op": "add",
        "path": "/timezone",
        "value": "Asia/Calcutta"
    }, // Contact timezone

    // -------------------------------
    // 3. Location Information
    // -------------------------------
    {
        "op": "remove",
        "path": "/address",
        "value": "Address field"
    }, // Street or full address
    {
        "op": "add",
        "path": "/city",
        "value": "pune"
    }, // City
    {
        "op": "add",
        "path": "/state",
        "value": "MH"
    }, // State
    {
        "op": "replace",
        "path": "/country",
        "value": "IN"
    }, // Country code
    {
        "op": "add",
        "path": "/zipcode",
        "value": "412410"
    }, // Postal code

    // -------------------------------
    // 4. Social Profiles
    // -------------------------------
    {
        "op": "add",
        "path": "/facebook",
        "value": "http://patchupdatefacebook.com"
    }, // Facebook profile URL
    {
        "op": "add",
        "path": "/twitter",
        "value": "http://patchupdatetwitter.com"
    }, // Twitter profile URL
    {
        "op": "add",
        "path": "/linkedin",
        "value": "http://patchupdatelinkedin.com"
    }, // LinkedIn profile URL

    // -------------------------------
    // 5. Professional Information
    // -------------------------------
    {
        "op": "add",
        "path": "/company",
        "value": 222911
    }, // Associated company ID
    {
        "op": "add",
        "path": "/companyCountry",
        "value": "AD"
    }, // Country of company
    {
        "op": "add",
        "path": "/designation",
        "value": "Product engineer"
    }, // Job title / designation
    {
        "op": "add",
        "path": "/department",
        "value": "engineering"
    }, // Department name
    {
        "op": "replace",
        "path": "/stakeholder",
        "value": true
    }, // Decision maker flag

    // -------------------------------
    // 6. Campaign Information
    // -------------------------------
    {
        "op": "replace",
        "path": "/source",
        "value": 479488
    }, // Marketing source ID
    {
        "op": "replace",
        "path": "/campaign",
        "value": 479487
    }, // Campaign ID
    {
        "op": "add",
        "path": "/subSource",
        "value": "updated by patch subSource"
    }, // Sub-source (additional campaign tracking)
    {
        "op": "add",
        "path": "/utmSource",
        "value": "updated by patch utmSource"
    }, // UTM source for analytics
    {
        "op": "add",
        "path": "/utmCampaign",
        "value": "updated by patch utmCampaign"
    }, // UTM campaign name
    {
        "op": "add",
        "path": "/utmMedium",
        "value": "updated by patch utmMedium"
    }, // UTM medium
    {
        "op": "add",
        "path": "/utmContent",
        "value": "updated by patch utmContent"
    }, // UTM content
    {
        "op": "add",
        "path": "/utmTerm",
        "value": "updated by patch utmTerm"
    }, // UTM term

    // -------------------------------
    // 7. Custom Fields
    // -------------------------------
    {
        "op": "add",
        "path": "/customFieldValues/cfTextFieldTest",
        "value": "updated by patch"
    }, // Text field
    {
        "op": "add",
        "path": "/customFieldValues/cfParagraphTextTest",
        "value": "Add paragraph description"
    }, // Paragraph / multi-line text
    {
        "op": "add",
        "path": "/customFieldValues/cfNumberTest",
        "value": 13
    }, // Number field
    {
        "op": "add",
        "path": "/customFieldValues/cfUrlFieldTest",
        "value": "https://app.kylas.io/"
    }, // URL field
    {
        "op": "add",
        "path": "/customFieldValues/cfDateTest",
        "value": "2023-12-13T06:30:00.000Z"
    }, // Date field
    {
        "op": "add",
        "path": "/customFieldValues/cfCheckboxTest",
        "value": true
    }, // Checkbox field (boolean)
    {
        "op": "add",
        "path": "/customFieldValues/cfDateTimePickerTest",
        "value": "2023-12-13T11:30:00.000Z"
    }, // Date & time picker

    // -------------------------------
    // 8. Multi-value & Picklist Fields
    // -------------------------------
    // Note:
    // 1. When adding a Multipicklist value for the first time, initialize with an empty array.
    // 2. If values already exist, do not re-initialize with an empty array.
    {
        "op": "add",
        "path": "/customFieldValues/cfMultipicklist",
        "value": []
    }, // Initialize multipicklist first time
    {
        "op": "add",
        "path": "/customFieldValues/cfMultipicklist/0",
        "value": 648461
    }, // Add first value
    {
        "op": "add",
        "path": "/customFieldValues/cfMultipicklist/1",
        "value": 648462
    }, // Add second value
    {
        "op": "add",
        "path": "/customFieldValues/cfMultipicklist/2",
        "value": 648463
    }, // Add third value
    {
        "op": "add",
        "path": "/customFieldValues/cfPickListTest",
        "value": 486042
    } // Single select picklist
]
```

## Company APIs

#### Create Company
`POST https://api.kylas.io/v1/companies/`

Create company API creates company with required values as below. Review below snippet and set values are per your requirement, Whichever value is not required, set null
API KEY can be found here
Custom field values should be placed in customFieldValues object as below
"customFieldValues": {
        "cfcustomfield":"this is custom field"
    }
Below is the sample request payload
{
    "name": "Shakti Pvt ltd",
    "numberOfEmployees": {
        "id": 79,
        "name": "1-4",
        "systemDefault": true
    },
    "annualRevenue": {
        "currencyId": 431,
        "value": 10000000
    },
    "website": "https://www.shakticorp.com",
    "industry": {
        "id": 571,
        "name": "Computer Software",
        "systemDefault": true
    },
    "businessType": {
        "id": 69,
        "name": "Analyst",
        "systemDefault": true
    },
    "emails": [
        {
            "type": "OFFICE",
            "value": "shakti@mailinator.com",
            "primary": true
        }
    ],
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "dialCode": "+91",
            "value": "9999999999",
            "primary": true
        }
    ],
    "timezone": {
        "id": 372,
        "name": "(GMT+05:30) Chennai, Kolkata, Mumbai, New Delhi / Sri Jayawardenapura",
        "systemDefault": true
    },
    "address": "601, Sarvodaya building, Behrambagh, Jogeshwari West",
    "city": "Mumbai",
    "state": "Maharashtra",
    "zip

```json
{
    "name": "Shakti Pvt ltd",
    "numberOfEmployees": {
        "id": 79,
        "name": "1-4",
        "systemDefault": true
    },
    "annualRevenue": {
        "currencyId": 431,
        "value": 10000000
    },
    "website": "https://www.shakticorp.com",
    "industry": {
        "id": 571,
        "name": "Computer Software",
        "systemDefault": true
    },
    "businessType": {
        "id": 69,
        "name": "Analyst",
        "systemDefault": true
    },
    "emails": [
        {
            "type": "OFFICE",
            "value": "shakti@mailinator.com",
            "primary": true
        }
    ],
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "dialCode": "+91",
            "value": "9999999999",
            "primary": true
        }
    ],
    "timezone": {
        "id": 372,
        "name": "(GMT+05:30) Chennai, Kolkata, Mumbai, New Delhi / Sri Jayawardenapura",
        "systemDefault": true
    },
    "address": "601, Sarvodaya building, Behrambagh, Jogeshwari West",
    "city": "Mumbai",
    "state": "Maharashtra",
    "zipcode": "400102",
    "country": {
        "id": 175,
        "name": "India",
        "systemDefault": true
    },
    "facebook": "https://www.fb,com",
    "twitter": "https://www.ty,com",
    "linkedIn": "https://www.li,com",
    "customFieldValues": {}
}
```

#### Update Company
`PUT http://api.kylas.io/v1/companies/<company_id>`

Update Company currently is a PUT request and It is a 3 step process for now

Fetch company details using 'Get company details' API.
From above request's response, update those fields which you want.
Copy paste the new payload in Update company request's body and hit 'Send'.

API KEY can be found here
Company ID can be found in company details page url.
Find Ids as below:

For any form field details like picklist value ids, Company type ids, Campaign, Source, any Custom fields and their value ids visit here

```json
{
  "name": "Acmeh Corp",
  "numberOfEmployees": {
    "id": 83,
    "name": "50-99"
  },
  "annualRevenue": {
    "currencyId": 431,
    "value": 6554440000
  },
  "website": "https://compweb.com/",
  "industry": {
    "id": 610,
    "name": "Information Technology and Services"
  },
  "businessType": {
    "id": 72,
    "name": "Integrator"
  },
  "emails": [
    {
      "type": "OFFICE",
      "value": "xyz@gmail.com",
      "primary": true
    },
    {
      "type": "OFFICE",
      "value": "erp@gmail.com",
      "primary": false
    }
  ],
  "phoneNumbers": [
    {
      "type": "MOBILE",
      "code": "IN",
      "dialCode": "+91",
      "value": "9877878767",
      "primary": true
    },
    {
      "type": "MOBILE",
      "code": "IN",
      "dialCode": "+91",
      "value": "9877868767",
      "primary": false
    }
  ],
  "timezone": {
    "id": 372,
    "name": "(GMT+05:30) Chennai, Kolkata, Mumbai, New Delhi / Sri Jayawardenapura"
  },
  "dnd": true,
  "address": "Twin Towers",
  "city": "Thane",
  "country": {
    "id": 175,
    "name": "India"
  },
  "state": "Maharashtra",
  "zipcode": "400605",
  "facebook": "https://compweb.com/",
  "twitter": "https://compweb.com/",
  "linkedIn": "https://compweb.com/"
}
```

#### Delete Company
`DELETE https://api.kylas.io/v1/companies/<company_id>`

Delete company using this API

```json
{}
```

#### Get Company Details
`GET https://api.kylas.io/v1/companies/<company_id>`

Get Company details API will fetch all the company details.
API KEY can be found here
Enter company_id in request URL whose details are to be fetched.
Sample response snippet below:
{
    "hasLogo": false,
    "id": 75212,
    "name": "company_1629820010143",
    "numberOfEmployees": null,
    "annualRevenue": null,
    "website": null,
    "industry": null,
    "businessType": null,
    "emails": [],
    "phoneNumbers": [],
    "timezone": null,
    "dnd": false,
    "address": null,
    "city": null,
    "country": null,
    "state": null,
    "zipcode": null,
    "facebook": null,
    "twitter": null,
    "linkedIn": null,
    "createdBy": {
        "id": 1,
        "name": "Gaurav Shinde"
    },
    "createdAt": "2022-11-17T17:17:08Z",
    "updatedAt": "2022-12-22T16:08:53Z",
    "updatedBy": {
        "id": 1,
        "name": "Gaurav Shinde"
    },
    "recordActions": {
        "read": true,
        "update": true,
        "quotation": true,
        "meeting": true,
        "document": true
    },
    "customFieldValues": null,
    "createdViaId": "1",
    "createdViaName": "User",
    "createdViaType": "Web",
    "updatedViaId": "1",
    "updatedViaName": "User",
    "updatedViaType": "Web",
    "importedBy": {
        "id": 1,
        "name": "Gaurav Shinde"
    },
    "ownedBy": {
        "id": 4,
        "name": "Uday Chouhan"
    }
}

#### Fetch Companies
`POST https://api.kylas.io/v1/search/company?page=0&size=100`

```json
{
    "fields": [
        "name",
        "ownedBy",
        "annualRevenue",
        "industry",
        "numberOfEmployees",
        "emails",
        "phoneNumbers",
        "city",
        "state",
        "country",
        "cfCustomPick",
        "companyPicklist",
        "id",
        "customFieldValues"
    ],
    "jsonRule": null
}
```

#### Update Company patch
`PATCH https://api.kylas.io/v1/companies/{{CompanyId}}`

```json
[
    // ---------------------------------------------------------
    // General Information
    // ---------------------------------------------------------
    {
        "op": "replace",
        "path": "/ownedBy",
        "value": {
            "name": "Sara Wilson",
            "id": 11622
        }
    },
    {
        "op": "replace",
        "path": "/name",
        "value": "Name Updated by Patch"
    },
    {
        "op": "add",
        "path": "/numberOfEmployees",
        "value": {
            "id": 41033,
            "name": "50-99"
        }
    },
    {
        "op": "remove",
        "path": "/annualRevenue"
    },
    {
        "op": "add",
        "path": "/website",
        "value": "https://app.kylas.io/"
    },
    {
        "op": "add",
        "path": "/industry",
        "value": {
            "id": 479289,
            "name": "Accounting"
        }
    },
    {
        "op": "add",
        "path": "/businessType",
        "value": {
            "id": 41039,
            "name": "Competitor"
        }
    },
    {
        "op": "add",
        "path": "/uniqueText1",
        "value": "2038fcc5-b85c-49cb-b46e-ef9da2aae431"
    },
    {
        "op": "replace",
        "path": "/uniqueText2",
        "value": "b85a297a-92d6-4a63-b66a-ab263646284d"
    },
    // ---------------------------------------------------------
    // Communication
    // ---------------------------------------------------------
    // Email
    // Note: You cannot perform replace operation if the Email field is empty.
    // You cannot mark all emails and phone numbers as primary = false.
    // At least one email and one phone number must remain primary in the system.
    {
        "op": "add",
        "path": "/emails/0",
        "value": {
            "type": "OFFICE",
            "value": "updatedbypatch1@gmail.com",
            "primary": false
        }
    },
    {
        "op": "add",
        "path": "/emails/1",
        "value": {
            "type": "OFFICE",
            "value": "updatedbypatch@gmail.com",
            "primary": false
        }
    },
    // PhoneNumber
    // Note: You cannot perform replace operation if the phone number field is empty.
    {
        "op": "add",
        "path": "/phoneNumbers/0",
        "value": {
            "id": null,
            "type": "MOBILE",
            "code": "IN",
            "value": "8734523499",
            "dialCode": "+91",
            "primary": false
        }
    },
    {
        "op": "add",
        "path": "/phoneNumbers/1",
        "value": {
            "id": null,
            "type": "MOBILE",
            "code": "IN",
            "value": "8734523487",
            "dialCode": "+91",
            "primary": false
        }
    },
    // Timezone
    {
        "op": "add",
        "path": "/timezone",
        "value": {
            "id": 372,
            "name": "(GMT+05:30) Chennai, Kolkata, Mumbai, New Delhi / Sri Jayawardenapura"
        }
    },
    // ---------------------------------------------------------
    // Location
    // ---------------------------------------------------------
    {
        "op": "replace",
        "path": "/address",
        "value": "Address Updated by Patch"
    },
    {
        "op": "replace",
        "path": "/city",
        "value": "City Udated by Patch"
    },
    {
        "op": "replace",
        "path": "/state",
        "value": "State Udated by Patch"
    },
    {
        "op": "replace",
        "path": "/zipcode",
        "value": "Zipcode Udated by Patch"
    },
    {
        "op": "add",
        "path": "/country",
        "value": {
            "id": 175,
            "name": "India"
        }
    },
    {
        "op": "add",
        "path": "/addressCoordinate",
        "value": {
            "lat": 18.5009698,
            "lon": 73.9429625
        }
    },
    // ---------------------------------------------------------
    // Social
    // ---------------------------------------------------------
    {
        "op": "replace",
        "path": "/facebook",
        "value": "http://patchupdatefacebook.com"
    },
    {
        "op": "remove",
        "path": "/twitter"
    },
    {
        "op": "remove",
        "path": "/linkedIn"
    },
    // ---------------------------------------------------------
    // Custom Fields (Other Details)
    // ---------------------------------------------------------
    //Custom_Fields
    // Note: You cannot perform replace operation if the field is empty.
    // Text field
    {
        "op": "add",
        "path": "/customFieldValues/cfTextField",
        "value": "updated by patch"
    },
    // Paragraph field
    {
        "op": "add",
        "path": "/customFieldValues/cfParagraphText",
        "value": "updated by patch"
    },
    // Number
    {
        "op": "add",
        "path": "/customFieldValues/cfNumber",
        "value": 11111
    },
    // Pick List
    {
        "op": "add",
        "path": "/customFieldValues/cfPickListTest",
        "value": {
            "id": 44318,
            "name": "Monday"
        }
    },
    // Initialise customFieldValues root if needed
    // ---------------- Multi Value Custom Field ----------------
    //Multivalue_Custom_Picklist 
    // Note:
    // 1. When adding Multipicklist Value first time you must initialise with empty array.
    // 2. When values already exist then do NOT initialise with empty array.
    {
        "op": "add",
        "path": "/customFieldValues",
        "value": {}
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiPickList",
        "value": []
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiPickList/0",
        "value": {
            "id": 52562,
            "name": "Wednesday"
        }
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiPickList/1",
        "value": {
            "id": 52561,
            "name": "Tuesday"
        }
    },
    {
        "op": "add",
        "path": "/customFieldValues/cfMultiPickList/2",
        "value": {
            "id": 52560,
            "name": "Monday"
        }
    },
    // Checkbox
    {
        "op": "add",
        "path": "/customFieldValues/cfCheckboxTest",
        "value": true
    },
    // Date Time Picker
    {
        "op": "add",
        "path": "/customFieldValues/cfDateTime",
        "value": "2023-12-13T11:30:00.000Z"
    },
    // Date
    {
        "op": "add",
        "path": "/customFieldValues/cfDate",
        "value": "2023-12-13T06:30:00.000Z"
    },
    // URL Field
    {
        "op": "add",
        "path": "/customFieldValues/cfUrlField",
        "value": "https://app.kylas.io/"
    }
 ]
```

## Call Log APIs

#### Create Call log on Lead
`POST https://api.kylas.io/v1/call-logs/`

This API is used to create call log on lead
Sample request payload:
'outcome' key can have values 'connected', 'missed', 'rejected', 'busy' and 'no_answer'
For all the above types other than connected, remove 'duration' key
{
    "outcome": "connected",
    "startTime": "2022-09-05T06:56:29.695Z",
    "phoneNumber": "9618488578",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "id": 297573,
        "entity": "lead",
        "phoneNumber": "9618488578"
    },
    "callRecording": {
        "fileName": "call.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}

```json
{
    "outcome": "connected",
    "startTime": "2022-09-05T06:56:29.695Z",
    "phoneNumber": "9618488578",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "id": 297573,
        "entity": "lead",
        "phoneNumber": "9618488578"
    },
    "callRecording": {
        "data": "",
        "fileName": "call.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}
```

#### Create Call log on Deal
`POST https://api.kylas.io/v1/call-logs/`

This API is used to create call log on lead
Sample request payload:
'outcome' key can have values 'connected', 'missed', 'rejected', 'busy' and 'no_answer'
For all the above types other than connected, remove 'duration' key
{
    "outcome": "connected",
    "startTime": "2022-09-02T07:59:21.902Z",
    "phoneNumber": "9848022338",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "id": 25633,
        "entity": "deal",
        "phoneNumber": "9848022338"
    },
    "associatedTo": [
        {
            "id": 112936,
            "entity": "contact",
            "phoneNumber": "9848022338"
        }
    ],
    "callRecording": {
        "data": "",
        "fileName": "sampel.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}

```json
{
    "outcome": "connected",
    "startTime": "2022-09-02T07:59:21.902Z",
    "phoneNumber": "9848022338",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "id": 25633,
        "entity": "deal",
        "phoneNumber": "9848022338"
    },
    "associatedTo": [
        {
            "id": 112936,
            "entity": "contact",
            "phoneNumber": "9848022338"
        }
    ],
    "callRecording": {
        "data": "",
        "fileName": "sampel.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}
```

#### Create Call log on Contact
`POST https://api.kylas.io/v1/call-logs/`

```json
{
    "outcome": "connected",
    "startTime": "2022-09-02T08:05:44.370Z",
    "phoneNumber": "9848022338",
    "callType": "outgoing",
    "duration": "420",
    "notes": [
        {
            "description": "Test note 1"
        },
        {
            "description": "Test note 2"
        }
    ],
    "relatedTo": {
        "entity": "contact",
        "id": 112936,
        "phoneNumber": "9848022338"
    },
    "callRecording": {
        "data": "",
        "fileName": "sampel.mp3",
        "url": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3"
    }
}
```

#### Update Call log Patch request
`PATCH https://api.kylas.io/v1/call-logs/<call_log_id>`

```json
{
 "relatedTo": 
        {
            "id": 1715,
            "entity": "contact",
            "name": "Pratik Chavan Kylas",
            "phoneNumber": "9999911111"
        }
}
```

#### Update Call log PUT request
`PUT https://api.kylas.io/v1/call-logs/<call_log_id>`

```json
{
    "outcome": "connected",
    "startTime": "2021-06-06T04:30:00.000Z",
    "phoneNumber": "+919877878767",
    "callType": "outgoing",
    "duration": 420,
    "relatedTo": 
        {
            "id": 76275,
            "entity": "lead",
            "name": "Miss. Pratik Waghmare",
            "phoneNumber": "9877878767"
        }
    ,
    "notes": [
        
    ],
    "associatedTo": [
       
    ],
    "callRecording": {
       
    }
}
```

#### Fetch Call logs on Contact
`GET https://api.kylas.io/v1/call-logs/<contact_id>?relatedToType=contact`

#### Fetch Call logs on Lead
`GET https://api.kylas.io/v1/call-logs/<lead_id>?relatedToType=lead`

#### Fetch Call logs on Deal
`GET https://api.kylas.io/v1/call-logs/<deal_id>?relatedToType=deal`

#### Sync call log
`POST https://api.kylas.io/v1/call-logs/sync`

```json
{
    "outcome": "connected",
    "startTime": "2025-03-030T01:40:00.000Z",
    "endTime": "2025-03-30T01:42:00.000Z",
    "remoteId": "139467692",
    "callType": "outgoing",
    "duration": 60,
    "ownerId": 3392,
    "originator": "+918655449417",
    "receiver": "+919999911111",
    //"callRecording": "https://voicelogic.com/wp-content/uploads/2017/04/hottransfer417500.mp3",//Add your recording url
    //"pickDuration": 10,
    "deviceId": null
}
```

#### List Call log
`POST https://api.kylas.io/v1/call-logs/`

```json
{
    "outcome": "connected",
    "startTime": "2021-05-05T06:30:00.000Z",
    "phoneNumber": "7447631718",
    "callType": "outgoing",
    "duration": 5566,
    "isManual": true,
    "owner": {
        "id": 119,
        "name": "Pratik Chavan",
        "phoneNumber": null
    },
    "relatedTo": [
        {
            "id": 64824,
            "entity": "lead",
            "name": "Mr. Rohit Chawda",
            "phoneNumber": "7447631718"
        }
    ],
    "associatedTo": [],
    "callRecording": null,
    "notes": [
        {
            "id": 314,
            "description": "Testing",
            "createdBy": {
                "id": 119,
                "name": "Pratik Chavan",
                "phoneNumber": null
            }
        }
    ]
}
```

#### Fetch Call Log Notes
`GET https://api.kylas.io/v1/notes/relation?page=0&size=10&targetEntityId={{CallLogID}}&targetEntityType=CALL_LOG&targetEntityOwnerId={{OwnerID}}`

#### Create Note On Call Log
`POST https://api.kylas.io/v1/notes/relation`

```json
{
    "sourceEntity": {
        "description": "<div>Add Your Note Contente here</div>",
        "mentions": null
    },
    "targetEntityId": {{Enter Call Log ID}},
    "targetEntityType": "CALL_LOG"
}
```

#### Delete Note from Call log
`DELETE https://api.kylas.io/v1/notes/{{Note ID}}?targetEntityType=CALL_LOG&targetEntityId={{CallLog ID}}`

## Meeting APIs

#### Create Meeting
`POST https://api.kylas.io/v1/meetings/search?page=1&size=100&sort=from,asc`

```json
{
    "title": "Enter Your Meeting Title Here",
    "allDay": false,
    "timezone": {
        "id": 372,
        "name": "Asia/Calcutta"
    },
    "relatedTo": [],
    "participants": [
        {
            "id": 2530,
            "entity": "user"
        }
    ],
    "from": "2022-08-26T08:00:00.000Z",
    "to": "2022-08-26T08:30:00.000Z"
}
```

#### Get All Meetings
`POST https://api.kylas.io/v1/meetings/search?page=1&size=100&sort=from,asc`

```json
{
   "title": "Test create meeting",
  "description": "Testing create meeting through api",
  "from": "2021-05-06T18:30:00.000Z",
  "to": "2021-05-06T19:00:00.000Z",
  "allDay": false,
  "location": "Pune",
  "createdAt": "2021-05-06T07:50:24.981Z",
  "updatedAt": "2021-05-06T07:50:24.981Z",
  "timezone": {
    "id": 372,
    "entity": "timezone",
    "name": "Asia/Calcutta"
  },
  "owner": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "createdBy": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "updatedBy": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "participants": [
    {
      "id": 411,
      "entity": "user",
      "name": "dc marvel",
      "email": "horanef498@aramidth.com",
      "rsvpResponse": null,
      "rsvpMessage": null
    },
    {
      "id": 119,
      "entity": "user",
      "name": "Pratik Chavan",
      "email": "pratik.chavan@kylas.io",
      "rsvpResponse": null,
      "rsvpMessage": null
    }
  ],
  "relatedTo": [
    {
      "id": 150,
      "entity": "contact",
      "name": "saniam tipu",
      "email": null
    },
    {
      "id": 169,
      "entity": "deal",
      "name": "Test Api"
    },
    {
      "id": 64824,
      "entity": "lead",
      "name": "Rohit Chawda",
      "email": "akshaygunshetti941998@gmail.com"
    }
  ]
   
}
```

#### Get Meeting Details
`GET https://api.kylas.io/v1/meetings/<meeting_id>`

#### Cancel meeting
`POST https://api.kylas.io/v1/meetings/<meeting_id>/cancel`

```json
{
   "title": "Test Edit meeting",
  "description": "Testing create meeting through api",
  "from": "2021-05-06T18:30:00.000Z",
  "to": "2021-05-06T19:00:00.000Z",
  "allDay": false,
  "location": "Pune",
  "createdAt": "2021-05-06T07:50:24.981Z",
  "updatedAt": "2021-05-06T07:50:24.981Z",
  "timezone": {
    "id": 372,
    "entity": "timezone",
    "name": "Asia/Calcutta"
  },
  "owner": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "createdBy": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "updatedBy": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "participants": [
    {
      "id": 411,
      "entity": "user",
      "name": "dc marvel",
      "email": "horanef498@aramidth.com",
      "rsvpResponse": null,
      "rsvpMessage": null
    },
    {
      "id": 119,
      "entity": "user",
      "name": "Pratik Chavan",
      "email": "pratik.chavan@kylas.io",
      "rsvpResponse": null,
      "rsvpMessage": null
    }
  ],
  "relatedTo": [
    {
      "id": 150,
      "entity": "contact",
      "name": "saniam tipu",
      "email": null
    },
    {
      "id": 169,
      "entity": "deal",
      "name": "Test Api"
    },
    {
      "id": 64824,
      "entity": "lead",
      "name": "Rohit Chawda",
      "email": "akshaygunshetti941998@gmail.com"
    }
  ]
   

}
```

#### Update Meetings
`PUT https://api.kylas.io/v1/meetings/<meeting_id>`

```json
{
   "title": "Test Edit meeting",
  "description": "Testing create meeting through api",
  "from": "2021-05-06T18:30:00.000Z",
  "to": "2021-05-06T19:00:00.000Z",
  "allDay": false,
  "location": "Pune",
  "createdAt": "2021-05-06T07:50:24.981Z",
  "updatedAt": "2021-05-06T07:50:24.981Z",
  "timezone": {
    "id": 372,
    "entity": "timezone",
    "name": "Asia/Calcutta"
  },
  "owner": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "createdBy": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "updatedBy": {
    "id": 119,
    "name": "Pratik Chavan"
  },
  "participants": [
    {
      "id": 411,
      "entity": "user",
      "name": "dc marvel",
      "email": "horanef498@aramidth.com",
      "rsvpResponse": null,
      "rsvpMessage": null
    },
    {
      "id": 119,
      "entity": "user",
      "name": "Pratik Chavan",
      "email": "pratik.chavan@kylas.io",
      "rsvpResponse": null,
      "rsvpMessage": null
    }
  ],
  "relatedTo": [
    {
      "id": 150,
      "entity": "contact",
      "name": "saniam tipu",
      "email": null
    },
    {
      "id": 169,
      "entity": "deal",
      "name": "Test Api"
    },
    {
      "id": 64824,
      "entity": "lead",
      "name": "Rohit Chawda",
      "email": "akshaygunshetti941998@gmail.com"
    }
  ]
   

}
```

#### Delete Meeting
`DELETE https://api.kylas.io/v1/meetings/<meeting_id>`

#### Fetch Meetings Notes
`GET https://api.kylas.io/v1/notes/relation?page=0&size=10&targetEntityId={{meetingid}}&targetEntityType=MEETING&targetEntityOwnerId={{OwnerID}}`

#### Create Note On Meetings
`POST https://api.kylas.io/v1/notes/relation`

```json
{
    "sourceEntity": {
        "description": "<div>Add Your Note Contente here</div>",
        "mentions": null
    },
    "targetEntityId": {{Enter Meeting ID}},
    "targetEntityType": "MEETING"
}
```

#### Delete Note from Meeting
`DELETE https://api.kylas.io/v1/notes/{{NoteID}}?targetEntityType=MEETING&targetEntityId={{MeetingID}}`

## Email APIs

#### Get Emails of thread
`GET https://api.kylas.io/v1/email-threads/3636/emails?entityId=<entity_id>&entityType=<entity_type>&page=1&size=10`

#### Get all emails
`GET https://api.kylas.io/v1/email-threads/3636/emails?entityId=51411&entityType=lead&page=1&size=10`

#### Download attachment
`GET https://api.kylas.io/v1/email-threads/3636/emails?entityId=51411&entityType=lead&page=1&size=10`

#### Send Email
`POST https://api.kylas.io/v1/emails/`

```json
{
    
            "from": {
                "id": 77199,
                "entity": "lead",
                "name": "Edit sharma 1629311016387",
                "email": "akshaygunshetti941998@gmail.com"
            },
            "to": [
                {
                    "id": 77199,
                    "entity": "lead",
                    "name": "Edit sharma 1629311016387",
                    "email": "akshaygunshetti941998@gmail.com"
                }
            ],
            "cc": [],
            "bcc": [
                {                    
                }
            ],
            "subject": "yes welcome lead  AD Gunceshetti",
            "body": "\u003cp\u003ewelcome to the team \u0026nbsp;\u0026lt;free text\u0026gt; AD\u003c/p\u003e",
            "sentAt": "2021-06-20T10:36:59.111Z",
            "read": true,
            "attachments": [
                {                    
                }
            ]        
 
}
```

#### Mark email as Read
`POST https://api.kylas.io/v1/emails/4823/mark_as_read`

#### Mark email as UnRead
`POST https://api.kylas.io/v1/emails/`

```json
{
    
            "from": {
                "id": 119,
                "entity": "user",
                "name": "Pratik Chavan",
                "email": "pratik.chavan@kylas.io"
            },
            "to": [
                {
                    "id": 65196,
                    "entity": "lead",
                    "name": "AD Gunceshetti",
                    "email": "pratik25ch@gmail.com"
                }
            ],
            "cc": [],
            "bcc": [
                {
                    "id": 0,
                    "entity": "customemail",
                    "name": "kireeti.annamaraj@kylas.io",
                    "email": "kireeti.annamaraj@kylas.io"
                }
            ],
            "subject": "yes welcome lead  AD Gunceshetti",
            "body": "\u003cp\u003ewelcome to the team \u0026nbsp;\u0026lt;free text\u0026gt; AD\u003c/p\u003e",
            "sentAt": "2021-06-20T10:36:59.111Z",
            "read": true,
            "attachments": [
                {
                    "id": 1490,
                    "fileName": "MicrosoftTeams-image (17)_1617185651.png",
                    "fileSize": 86125
                }
            ]        
 
}
```

## Products and Services APIs

#### Create Product and Service
`POST https://api.kylas.io/v1/products`

```json
{
	"isActive": true,
	"name": "{{prd_name}}",
	"price": {
		"currencyId": 431,
		"value": {{price}}
	},
	"customFieldValues": {}
}
```

#### Deactivate Product and Service
`PUT https://api.kylas.io/v1/products/<product_id>`

Deactivate product using this API
Sample payload
{
    "id": 22526,
    "name": "bahraini dinar",
    "price": {
        "currencyId": 401938,
        "value": 20
    },
    "description": null,
    "isActive": false
}

```json
{
    "id": 22526,
    "name": "bahraini dinar",
    "price": {
        "currencyId": 401938,
        "value": 20
    },
    "description": null,
    "isActive": false
}
```

#### Update Product and Service
`PUT https://api.kylas.io/v1/products/<product_id>`

```json
{
    "id": 41969,
    "name": "prd_name_update",
    "price": {
        "currencyId": 431,
        "value": 2001
    },
    "description": "desc update",
    "isActive": true,
    "createdAt": "2022-09-08T06:34:46Z",
    "updatedAt": "2022-09-08T06:34:46Z",
    "customFieldValues": {}
}
```

#### Get products  ids, Names
`POST https://api.kylas.io/v1/products/summary`

```json
{
    "valid": true,
    "condition": "AND",
    "rules": [
        {
            "id": "id",
            "field": "id",
            "type": "double",
            "operator": "in",
            //Add your product id's below to get the deatils 
            "value": "{{Add product id's}}"
        }
    ]
}
```

## Reports APIs

#### Fetch All Reports
`GET https://api.kylas.io/v3/reports/search?page=0&size=100`

Fetch Reports API fetches all reports
API KEY can be found here

#### Get Report Details
`GET https://api.kylas.io/v3/reports/<report_id>`

Fetch Report details API fetches the  details of the report. You can find the report id from report url
API KEY can be found here

#### Delete Report
`DELETE https://api.kylas.io/v3/reports/<report_id>`

Delete unwanted report using Delete API. You can find the report id from report url
API KEY can be found here

## Task APIs

#### Create Task
`POST https://api.kylas.io/v1/tasks/`

```json
{
	"type": 12662,
	"status": 12666,
	"reminder": "ONE_HOUR",
	"assignedTo": 830,
	"dueDate": "2022-12-24T14:00:00.000Z",
	"name": "{{date_time}}",
	"customFieldValues": {}
}
```

#### Get Task Details
`GET https://api.kylas.io/v1/tasks/<task_id>`

#### Update Task
`PUT https://api.kylas.io/v1/tasks/<task_id>`

```json
{
    "name": "Edit_Task_1632377320933",
    "dueDate": "2022-11-24T14:00:00.000+0000",
    "type": 20272,
    "status": 20275,
    "priority": 20278,
    "reminder": "THIRTY_MINUTES",
    "assignedTo":830
}
```

#### Get all Task fields
`GET https://api.kylas.io/v1/ui/layouts/CREATE/TASK`

```json
{
  "firstName": "Pratik",
  "lastName": "Waghmar",
  "pipeline": 834,
  "phoneNumbers": [
    {
      "type": "MOBILE",
      "code": "IN",
      "value": "09877878767",
      "dialCode": "+91",
      "primary": true
    },
    {
      "type": "MOBILE",
      "code": "IN",
      "value": "09877888767",
      "dialCode": "+91",
      "primary": false
    }
  ],
  "salutation": 996,
  "emails": [
    {
      "type": "OFFICE",
      "value": "abhishek.chouhan@kylas.io",
      "primary": true
    },
    {
      "type": "OFFICE",
      "value": "addemail@mailinator.com",
      "primary": false
    },
    {
      "type": "OFFICE",
      "value": "kylastesing25@gmail.com",
      "primary": false
    }
  ],
  "timezone": "Etc/GMT+12",
  "city": "Navi Mumbai",
  "state": "Maharashtra",
  "zipcode": "400605",
  "country": "IN",
  "department": "Technology",
  "dnd": true,
  "facebook": "https://www.facebook.com",
  "twitter": "https://www.facebook.com",
  "linkedIn": "https://www.facebook.com",
  "address": "112, Millenium Businesspark",
  "companyName": "doodle",
  "companyAddress": "Translab",
  "companyCity": "Mumbai",
  "companyState": "Maharashtra",
  "companyZipcode": "400506",
  "companyCountry": "IN",
  "companyEmployees": 2747,
  "companyAnnualRevenue": 5555555,
  "companyWebsite": "https://www.ggbuhiuj.com",
  "companyPhones": [
    {
      "type": "MOBILE",
      "code": "IN",
      "value": "09877878767",
      "dialCode": "+91",
      "primary": true
    }
  ],
  "companyIndustry": "BIOTECHNOLOGY",
  "companyBusinessType": "competitor",
  "requirementName": "Tera Byte ",
  "requirementCurrency": "GBP",
  "requirementBudget": 55555,
  "products": [
    {
      "id": 44,
      "name": "CRM - Gold"
    },
    {
      "id": 45,
      "name": "CRM - Diamond"
    },
    {
      "id": 87,
      "name": "CRM"
    },
    {
      "id": 42,
      "name": "Marketing Service"
    }
  ],
  "designation": "CEO",
  "campaign": 997,
  "source": 999,
  "conversionDetails": [],
  "customFieldValues": {
    "newCheckbox": true,
    "custom": "2021-03-10T06:30:00.000Z"
  }
}
```

#### Get Task Priority Ids
`GET https://api.kylas.io/v1/ui/layouts/list/task`

## Account Related APIs

#### Get Access Token from User creds
`PUT https://api.kylas.io/v1/users/login?view=access-token`

Fetch access token by giving user creds
Enter user credentials in body to fetch access token related to that account
Sample payload
{
    "email": "1632303804928@mailinator.com",
    "password": "Test@777"
}

```json
{
    "email": "1632303804928@mailinator.com",
    "password": "Test@777"
}
```

#### Fetch API Key from User creds
`GET https://api.kylas.io/v1/api-keys/kylas-app-key`

Fetch api-key using the bearer token as shown in this API

## Messages APIs Leads APIs

#### Create Messages with File URL
`POST https://api.kylas.io/v1/messages`

```json
{
    "content": "Stay in Touch: Go Beyond Checking In Let’s pretend you’re a customer. You recently purchased a product for your small business that requires additional service from a Big Company. You use their product on a daily basis and generally feel like Big Company does a good job at servicing you when you are having a problem with the product. You have a great relationship with the representative that has been assigned to your account. She sends frequent emails to keep a pulse on what challenges you might be having with the product and always gets you the answers to your questions in a timely manner.",
    "medium": "whatsapp",    
    "senderNumber": 7447631718,
    "recipientNumber": 8777667676,
    "direction": "outgoing",
    "sentAt": "2021-7-20T01:42:00.000Z",
    "status": "sent",
    "recipients": [
        {
            "entity": "lead",
            "id": 76677,
            "name": "test",
            "phoneNumber": "8777667676"
        }
    ],
    "relatedTo": [
        {
            "entity": "lead",
            "id": 77199,
            "name": "test"            
        }
    ], // In case of deal this will be deal
    //In case of deal this will be contact
    "attachments": [
        {
            "fileName": "b.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        },
        {
            "fileName": "bty.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        }
    ]
}
```

#### Create Messages with File URL Copy
`POST https://api.kylas.io/v1/messages`

```json
{
    "content": "Stay in Touch: Go Beyond Checking In Let’s pretend you’re a customer. You recently purchased a product for your small business that requires additional service from a Big Company. You use their product on a daily basis and generally feel like Big Company does a good job at servicing you when you are having a problem with the product. You have a great relationship with the representative that has been assigned to your account. She sends frequent emails to keep a pulse on what challenges you might be having with the product and always gets you the answers to your questions in a timely manner.",
    "medium": "whatsapp",
    "ownerId": 119,
    "senderNumber": 7447631718,
    "recipientNumber": 7877667656,
    "direction": "outgoing",
    "sentAt": "2021-7-20T01:42:00.000Z",
    "status": "sent",
    "recipients": [
         {
            "entity": "lead",
            "id": 77199,
            "name": "Wefwqef Hybjo",
            "phoneNumber": "7877656676"
        }
    ],
    "relatedTo": [
        {
            "entity": "lead",
            "id": 77199,
            "name": "Wefwqef Hybjo",
            "phoneNumber": "7877656676"
        }
    ], // In case of deal this will be deal
    //In case of deal this will be contact
    "attachments": [
        {
            "fileName": "b.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        },
        {
            "fileName": "bty.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        }
    ]
}
```

#### Create Messages with File data
`POST https://api.kylas.io/v1/messages`

#### Delete Messages
`DELETE https://api.kylas.io/v1/messages/146`

#### Sync Messages
`POST https://api.kylas.io/v1/messages/sync`

```json
{
    "content": "This is my message",
    "medium": "LInkedIn",
    "ownerId": 119,
    "remoteId": "iusdcndmsniosdvi",
    "direction": "outgoing",
    "status": "sent",
    "sentAt": "2021-11-10T01:42:00.000Z",
    "senderNumber": "8655449417",
    "recipientNumber": "8766765567",
    "attachments": [
        {
            "id": 116,
            "fileName": "b.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3",
            "_destroy": true
        },
        {
            "fileName": "b2.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        }
    ]
}
```

#### List Messages
`POST https://api.kylas.io/v1/messages/search?page=1&size=10`

```json
{
  "jsonRule": {
    "condition": "AND",
    "rules": [
      {
        "operator": "equal",
        "id": "related_to",
        "field": "related_to",
        "type": "related_look_up",
        "value": {
          "id": 76506,
          "entity": "lead"
        }
      }
    ]
  }
}
```

#### Get Message
`GET https://api.kylas.io/v1/messages/<message_id>`

## Messages APIs Deals APIs

#### Create Messages with File URL
`POST https://api.kylas.io/v1/messages`

```json
{
    "content": "Sure, Thank you. Will get back to you in sometime",
    "medium": "whatsapp",
    "ownerId": 830,
    "recipientNumber": 8655449417,    
    "senderNumber": 7447631718,
    "direction": "outgoing",
    "sentAt": "2021-7-20T01:42:00.000Z",
    "status": "sent",
    "relatedTo": [
        {
            "entity": "lead",
            "id": 77199,
            "name": "Wefwqef Hybjo",
            "phoneNumber": "7447631718" //Entity's number
        }
    ], // In case of deal this will be deal
    //In case of deal this will be contact
    "attachments": [
        {
            "fileName": "b.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        }
    ]
}
```

#### Create Messages with File data
`POST https://api.kylas.io/v1/messages`

#### Delete Messages
`DELETE https://api.kylas.io/v1/messages/<message_id>`

#### Sync Messages
`POST https://api.kylas.io/v1/messages/sync`

```json
{
    "content": "This is my message",
    "medium": "Whatsapp",
    "ownerId": 830,
    "remoteId": "testsakadkkm",
    "direction": "outgoing",
    "status": "read",
    "sentAt": "1020-11-20T01:42:00.000Z",
    "senderNumber": "8655449417",
    "recipientNumber": "8998497767",
    "attachments": [
        {
            "fileName": "b.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        },
        {
            "fileName": "b2.mp3",
            "url": "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"
        }
    ]
}
```

#### List Messages
`POST https:///api.kylas.io/v1/messages/search?page=1&size=10`

```json
{
  "jsonRule": {
    "condition": "AND",
    "rules": [
      {
        "operator": "equal",
        "id": "related_to",
        "field": "related_to",
        "type": "related_look_up",
        "value": {
          "id": 76506,
          "entity": "lead"
        }
      }
    ]
  }
}
```

#### Get Message
`GET https://api.kylas.io/v1/messages/<message_id>`

## Wokflow APIs

#### CreateWorkflow
`POST https://api.kylas.io/v1/workflows`

```json
{
	"name": "Lead_create_workflow 1",
	"description": "",
	"active": false,
	"actions": [{
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "firstName",
			"isStandard": true,
			"value": "fname_changed",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "lastName",
			"isStandard": true,
			"value": "lname_changed",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "pipeline",
			"isStandard": true,
			"value": {
				"id": 1493,
				"name": "Default Lead Pipeline",
				"stage": {
					"id": 10725,
					"name": "Open"
				}
			},
			"valueType": "OBJECT"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyIndustry",
			"isStandard": true,
			"value": "ACCOUNTING",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "timezone",
			"isStandard": true,
			"value": "Asia/Calcutta",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "country",
			"isStandard": true,
			"value": "IN",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "address",
			"isStandard": true,
			"value": "sample address",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "city",
			"isStandard": true,
			"value": "Mumbai",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "state",
			"isStandard": true,
			"value": "Maharashtra",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "zipcode",
			"isStandard": true,
			"value": "400102",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "facebook",
			"isStandard": true,
			"value": "https://www.fb.com",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "twitter",
			"isStandard": true,
			"value": "https://www.ty.com",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "linkedIn",
			"isStandard": true,
			"value": "https://www.li.com",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyName",
			"isStandard": true,
			"value": "Mumbai Indians",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "department",
			"isStandard": true,
			"value": "Engineering",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "designation",
			"isStandard": true,
			"value": "Master",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyBusinessType",
			"isStandard": true,
			"value": "competitor",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "dnd",
			"isStandard": true,
			"value": true,
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyEmployees",
			"isStandard": true,
			"value": 12648,
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyAnnualRevenue",
			"isStandard": true,
			"value": 100000000,
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyWebsite",
			"isStandard": true,
			"value": "https://www.mi.com",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyAddress",
			"isStandard": true,
			"value": "Company address",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyCity",
			"isStandard": true,
			"value": "Mumbai",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyState",
			"isStandard": true,
			"value": "Maharashtra",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyCountry",
			"isStandard": true,
			"value": "IN",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "companyZipcode",
			"isStandard": true,
			"value": "400102",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "requirementName",
			"isStandard": true,
			"value": "requirement",
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "campaign",
			"isStandard": true,
			"value": 12653,
			"valueType": "PLAIN"
		}
	}, {
		"type": "EDIT_PROPERTY",
		"payload": {
			"name": "source",
			"isStandard": true,
			"value": 12654,
			"valueType": "PLAIN"
		}
	}],
	"entityType": "LEAD",
	"trigger": {
		"name": "EVENT",
		"triggerFrequency": "CREATED"
	},
	"condition": {
		"conditionType": "FOR_ALL"
	}
}
```

## Dashboard APIs

#### Create Dashboard
`POST https://api.kylas.io/v1/dashboards`

```json
{
    "name": "Dashboard_name10",
    "sections": [
        {
            "order": 0,
            "entityType": "lead",
            "dashlets": [
                {
                    "row": 0,
                    "column": 0,
                    "dashletType": "smartlist",
                    "dashletContent": [
                        {
                            "id": 6996,
                            "name": "All converted leads",
                            "description": "All converted leads"
                        }
                    ]
                }
            ]
        }
    ]
}
```

#### Delete Dashboard
`DELETE https://api.kylas.io/v1/dashboards/<dashboard_id>`

#### Get list of Dashboards
`GET https://api.kylas.io/v1/dashboards`

#### Get Dashboards details
`GET https://api.kylas.io/v1/dashboards/<dashboard_id>`

#### Dashboard - Mark as Primary
`POST https://api.kylas.io/v1/dashboards/<dashboard_id>/mark_as_preferred`

## User Management APIs

#### Get Current User Details
`GET https://api.kylas.io/v1/users/me`

This API fetches user details
User id can be found in user details URL
Sample response
{"createdAt":"2022-07-28T14:58:12.721+0000","updatedAt":"2022-08-09T14:51:59.170+0000","createdBy":1,"updatedBy":1,"recordActions":{"read":true,"update":true,"delete":true,"email":false,"call":false,"sms":false,"task":false,"note":false,"meeting":false,"document":false,"deleteAll":false,"quotation":false},"metaData":{"idNameStore":{"updatedBy":{"1":"Gaurav Pasaarkar"},"createdBy":{"1":"Gaurav Pasaarkar"},"dateFormat":{},"profileId":{"3":"Restricted User"},"timezone":{},"currency":{},"language":{},"salutation":{},"ownerId":{"1":"Gaurav Pasaarkar"}}},"id":14804,"firstName":"user","lastName":"1659020292121","email":"1659020292121@maildrop.cc","updatedEmail":null,"salutation":null,"phoneNumbers":[{"type":"MOBILE","code":"IN","value":"9805215355","dialCode":"+91","primary":true}],"designation":null,"timezone":"Asia/Calcutta","language":"EN","dateFormat":"MMM D, YYYY [at] h:mm a","currency":"INR","signature":null,"title":null,"department":null,"failedAttempts":null,"locked":false,"lockedAt":null,"active":true,"deactivateReason":null,"emailVerified":true,"confirmedAt":null,"confirmationTokenSentAt":null,"resetPasswordTokenSentAt":null,"unlockTokenSentAt":null,"customFieldValues":{},"profileId":3,"permissions":[{"id":24,"name":"report","description":"has access to Reports","limits":5,"units":"count","action":{"read":true,"write":true,"update":true,"delete":true,"email":false,"call":false,"sms":fals

#### Get Any User Details
`GET https://api.kylas.io/v1/users/<user_id>`

#### Activate User
`PUT https://api.kylas.io/v1/users/<user_id>/activate`

#### Deactivate User
`PUT https://api.kylas.io/v1/users/<user_id>/deactivate`

#### Create User
`POST https://api.kylas.io/v1/users/invite`

```json
{
    "currency": "INR",
    "timezone": "Asia/Calcutta",
    "dateFormat": "MMM D, YYYY [at] h:mm a",
    "language": "EN",
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "dialCode": "+91",
            "value": "9090909090",
            "primary": true
        }
    ],
    "salutation": 703,
    "firstName": "Sharad",
    "lastName": "Pawar",
    "email": "sharad.pawar@mailinator.com",
    "designation": "Minister",
    "department": "State Cabinet",
    "profileId": 3,
    "signature": "sharad_bhau",
    "customFieldValues": {}
}
```

#### Update User
`PUT https://api.kylas.io/v1/users/<user_id>`

```json
{
    "createdAt": "2022-09-10T06:49:35.958+0000",
    "updatedAt": "2022-09-10T06:49:36.141+0000",
    "createdBy": 1,
    "updatedBy": 1,
    "id": 16945,
    "firstName": "Sharath",
    "lastName": "Pawar",
    "email": "sharad.pawar@mailinator.com",
    "updatedEmail": null,
    "salutation": 703,
    "phoneNumbers": [
        {
            "type": "MOBILE",
            "code": "IN",
            "value": "9090909090",
            "dialCode": "+91",
            "primary": true
        }
    ],
    "designation": "Minister",
    "timezone": "Asia/Calcutta",
    "language": "EN",
    "dateFormat": "MMM D, YYYY [at] h:mm a",
    "currency": "USD",
    "signature": "sharad_bhau",
    "title": null,
    "department": "State Cabinet",
    "failedAttempts": null,
    "locked": false,
    "lockedAt": null,
    "active": false,
    "deactivateReason": null,
    "emailVerified": false,
    "confirmedAt": null,
    "confirmationTokenSentAt": null,
    "resetPasswordTokenSentAt": null,
    "unlockTokenSentAt": null,
    "profileId": 3,
    "permissions": [
        {
            "id": 17,
            "name": "contact",
            "description": "has permission to contact resource",
            "limits": 50,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": true,
                "call": true,
                "sms": true,
                "task": true,
                "note": true,
                "meeting": true,
                "document": true,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": true
            }
        },
        {
            "id": 61,
            "name": "meeting",
            "description": "has access to Meetings",
            "limits": 5,
            "units": "count",
            "action": {
                "read": false,
                "write": false,
                "update": false,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 75,
            "name": "webhook",
            "description": "has access to Webhooks",
            "limits": 5,
            "units": "count",
            "action": {
                "read": false,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 13,
            "name": "profile",
            "description": "has permission to profile resource",
            "limits": 50,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 28,
            "name": "email_template",
            "description": "has access to Email Templates",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 11,
            "name": "shareRule",
            "description": "has permission to sharing a resource",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 66,
            "name": "export",
            "description": "has access to Export",
            "limits": 5,
            "units": "count",
            "action": {
                "read": false,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 6,
            "name": "customField",
            "description": "has access to custom field resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 18,
            "name": "company",
            "description": "has permission to contact resource",
            "limits": 50,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": true,
                "note": true,
                "meeting": true,
                "document": true,
                "readAll": true,
                "updateAll": false,
                "deleteAll": false,
                "quotation": true
            }
        },
        {
            "id": 77,
            "name": "document",
            "description": "has access to Documents",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 27,
            "name": "workflow",
            "description": "has access to Workflows",
            "limits": 5,
            "units": "count",
            "action": {
                "read": false,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 16,
            "name": "note",
            "description": "has permission to note resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 65,
            "name": "dashboard",
            "description": "has access to Dashboard",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 20,
            "name": "layout",
            "description": "has permission to layout resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 8,
            "name": "config",
            "description": "has access to tenant configuration resource",
            "limits": 100,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 25,
            "name": "lead-capture-forms",
            "description": "has access to Lead Capture Forms",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 12,
            "name": "deal",
            "description": "has permission to deal resource",
            "limits": 50,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": true,
                "call": true,
                "sms": true,
                "task": true,
                "note": true,
                "meeting": true,
                "document": true,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": true
            }
        },
        {
            "id": 15,
            "name": "task",
            "description": "has permission to task resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": true,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 24,
            "name": "report",
            "description": "has access to Reports",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 3,
            "name": "user",
            "description": "has access to user resource",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 63,
            "name": "call",
            "description": "has access to Calls",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 7,
            "name": "team",
            "description": "has access to team resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 10,
            "name": "pipeline",
            "description": "has access to pipeline resource",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 4,
            "name": "lead",
            "description": "has access to lead resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": true,
                "call": true,
                "sms": true,
                "task": true,
                "note": true,
                "meeting": true,
                "document": true,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 9,
            "name": "searchList",
            "description": "has access to search list resource",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 19,
            "name": "availability",
            "description": "has permission to availability resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": false,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 22,
            "name": "products-services",
            "description": "has access to Products and Services",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 14,
            "name": "conversionMapping",
            "description": "has permission to lead conversion mapping resource",
            "limits": -1,
            "units": "count",
            "action": {
                "read": true,
                "write": false,
                "update": true,
                "delete": false,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 62,
            "name": "email",
            "description": "has access to Emails",
            "limits": 5,
            "units": "count",
            "action": {
                "read": false,
                "write": false,
                "update": false,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 64,
            "name": "sms",
            "description": "has access to Sms",
            "limits": 5,
            "units": "count",
            "action": {
                "read": false,
                "write": false,
                "update": false,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        },
        {
            "id": 76,
            "name": "quotation",
            "description": "has access to Quotations",
            "limits": 5,
            "units": "count",
            "action": {
                "read": true,
                "write": true,
                "update": true,
                "delete": true,
                "email": false,
                "call": false,
                "sms": false,
                "task": false,
                "note": false,
                "meeting": false,
                "document": false,
                "readAll": false,
                "updateAll": false,
                "deleteAll": false,
                "quotation": false
            }
        }
    ],
    "emailProvider": null,
    "customFieldValues": {}
}
```

## Billing Related APIs

#### Get Usage Statistics
`GET https://api.kylas.io/v1/tenants/usage`

Use this API to fetch usage statistics on tenant level
Sample response
{
    "planName": "Elevate",
    "plan": {
        "id": "elevate-annual",
        "name": "Elevate"
    },
    "renewalAt": "2023-09-07T18:30:00.000+0000",
    "updatedAt": "2023-09-07T18:30:00.000+0000",
    "users": {
        "used": 20.0,
        "total": 9.223372036854776E15
    },
    "records": {
        "used": 45925.0,
        "total": 100000.0
    },
    "storage": {
        "used": 0.19,
        "total": 100.0
    },
    "workflows": {
        "used": 0.0,
        "total": 30.0
    },
    "emailTemplates": {
        "used": 0.0,
        "total": 30.0
    },
    "customFields": {
        "used": 22.0,
        "total": 25.0
    },
    "marketPlaceApps": {
        "used": 0.0,
        "total": 9.223372036854776E15
    },
    "dashboards": {
        "used": 0.0,
        "total": 1.7976931348623157E308
    },
    "entityCounts": [{
        "entity": "CALL",
        "count": 665
    }, {
        "entity": "MESSAGE",
        "count": 4
    }, {
        "entity": "EMAIL",
        "count": 587
    }, {
        "entity": "TASK",
        "count": 1369
    }, {
        "entity": "MEETING",
        "count": 312
    }, {
        "entity": "COMPANY",
        "count": 838
    }, {
        "entity": "LEAD",
        "count": 11587
    }, {
        "entity": "DEAL",
        "count": 20076
    }, {
        "entity": "CONTACT",
        "count": 10439
    }, {
        "entity": "NOTE",
        "count": 48
    }],
   

## Quotation APIs

#### Create Quotation
`POST https://api.kylas.io/v1/quotations/`

```json
{
    "currencyId": 431,
    "additionalDiscount": {
        "type": "PERCENTAGE",
        "value": 0
    },
    "additionalTax": 0,
    "adjustment": {
        "type": "PERCENTAGE",
        "value": 0
    },
    "isBillingAndShippingAddressSame": false,
    "status": {
        "id": "DRAFT",
        "name": "Draft"
    },
    "subTotal": 100000,
    "grandTotal": 100000,
    "summary": "Corporate Space 2000 sqft",
    "associatedDeal": {
        "id": "<deal id aginst which quotation is being created>"
            },
    "associatedContacts": [
        {
            "id": <associated contact id>
        }
    ],
    "associatedCompany": {
        "id": <associated company id>
    },
    "products": [
        {
            "id": <product id>,
            "quantity": 1,
            "price": {
                "currencyId": 431,
                "value": 100000
            },
            "discount": {
                "type": "PERCENTAGE",
                "value": 0
            },
            "tax": 0,
            "totalAmount": {
                "currencyId": 431,
                "value": 100000
            },
            "description": "<add product description here>"
        }
    ],
    "billingAddress": "<billing address>",
    "shippingAddress": "<shipping address>",
    "billingCity": "<billing city>",
    "shippingCity": "<shipping city>",
    "billingState": "<billing State>",
    "shippingState": "<shipping state>",
    "billingCountry": {
        "id": 175,
        "name": "India",
        "disabled": false
    },
    "shippingCountry": {
        "id": 175,
        "name": "India",
        "disabled": false
    },
    "billingPinCode": "<billing address zipcode>",
    "shippingPinCode": "<shipping address zipcode>"
    }
```

#### Update Quotation
`PUT https://api.kylas.io/v1/quotations/<quotation_id that is to be updated>`

```json
{
    "id": 22,
    "summary": "<quotation summary>",
    "currencyId": 431,
    "subTotal": 100000,
    "additionalTax": 0,
    "grandTotal": 100000,
    "isBillingAndShippingAddressSame": false,
    "status": {
        "id": "DRAFT",
        "name": "Draft"
    },
    "additionalDiscount": {
        "type": "PERCENTAGE",
        "currencyId": 431,
        "value": 0
    },
    "adjustment": {
        "type": "PERCENTAGE",
        "currencyId": 431,
        "value": 0
    },
    "associatedDeal": {
        "id": <associated_deal_id>
    },
    "associatedContacts": [
        {
            "id": <associated_contact_id>
        },
        {
            "id": <associated_contact_id>
        }
    ],
    "associatedCompany": {
        "id": <associated_company_id>
    },
    "products": [
        {
            "id": <product_id>,
            "name": "<Product Name>",
            "description": "<Product description>",
            "quantity": 1,
            "price": {
                "currencyId": 431,
                "value": <product_value>
            },
            "discount": {
                "type": "PERCENTAGE",
                "value": 0
            },
            "tax": 0,
            "totalAmount": {
                "currencyId": 431,
                "value": 100000
            }
        }
    ],
    "billingAddress": "<billing address>",
    "billingCity": "<billing city>",
    "billingCountry": {
        "id": 175,
        "name": "India"
    },
    "billingState": "<billing State>",
    "billingPinCode": "<billing address zipcode>",
    "shippingAddress": "<shipping address>",
    "shippingCity": "<shipping city>",
    "shippingState": "<shipping state>",
    "shippingPinCode": "<shipping address zipcode>",
    "shippingCountry": {
        "id": 175,
        "name": "India"
    }    
}
```

#### Delete Quotation
`DELETE https://api.kylas.io/v1/quotations/<quotation_id that is to be deleted>`

## Webhook APIs

#### Create Webhook
`POST https://api.kylas.io/v1/webhooks/`

```json
{
    "name": "sample webhook for lead",
    "requestType": "POST",
    "url": "https://webhook.site/2fb900a0-2d63-4c45-af3d-64e756768143",
    "authenticationType": "NONE",
    "authenticationKey": null,
    "events": [
        "LEAD_CREATED",
        "LEAD_UPDATED",
        "LEAD_DELETED"
    ],
    "active": true
}
```

#### Update Webhook
`PUT https://api.kylas.io/v1/webhooks/<webhook_id>`

```json
{
    "name": "sample webhook for lead",
    "requestType": "POST",
    "url": "https://webhook.site/2fb900a0-2d63-4c45-af3d-64e756768143",
    "authenticationType": "NONE",
    "authenticationKey": null,
    "events": [
        "LEAD_CREATED",
        "LEAD_UPDATED",
        "LEAD_DELETED",
        "CONTACT_CREATED",
        "CONTACT_UPDATED",
        "CONTACT_DELETED"
    ],
    "active": true
}
```

#### Delete Webhook
`DELETE {{env}}/webhooks/<webhook_id>`

## Import Scripts APIs

#### Import Companies
`POST https://api.kylas.io/v1/companies/`

Put the below code in Pre-requisite script to import data from csv file
var payload = {};

//company name
if (data["name"] != "") {
    payload["name"] = data["name"];
}

// city
if (data["city"] != "") {
    payload["city"] = data["city"];
}

// state
if (data["state"] != "") {
    payload["state"] = data["state"];
}

//address
if (data["address"] != "") {
    payload["address"] = data["address"];
}

// zipcode
if (data["zipcode"] != "") {
    payload["zipcode"] = data["zipcode"];
}

// phone numbers | if there are multiple phone numbers | rename columns as 'phone1', 'phone2' and 'phone3'

if (data["phone1"] != "") {
    // for number 1
    var phone1 = data["phone1"];
    var phone1_obj = {
        "type": "MOBILE",
        "dialCode": "+91",
        "code": "IN",
        "value": phone1,
        "primary": true
    }

    payload["phoneNumbers"] = [];
    payload["phoneNumbers"].push(phone1_obj);

    if (data["phone2"] != "") {

        var phone2 = data["phone2"];
        var phone2_obj = {
            "type": "MOBILE",
            "dialCode": "+91",
            "code": "IN",
            "value": phone2,
            "primary": false
        }
        payload["phoneNumbers"].push(phone2_obj);

        if (data["phone3"] != "") {

            var phone3 = data["phone3"];
            var phone3_obj = {
                "type": "MOBILE",
                "dialCode": "+91",
                "code": "IN",
                "value": phone3,
                "primary": false
         

```json
{{body}}
```

#### Import Contacts
`POST https://api.kylas.io/v1/contacts/`

Put the below script in pre-requisite section of postman request to import data from csv file
var payload = {};

//first name | Contact first name | Rename the column in sheet as 'Name'
if (data["Name"] != "") {
    payload["firstName"] = data["Name"];
}

//last name | Contact last name | Rename the column in sheet as 'surname'
if (data["surname"] != "") {
    payload["lastName"] = data["surname"];
}

// email | enter email column in sheet as 'email'
if (data["email"] != "") {
    var emailId = data["email"];
    var email = {
        "type": "OFFICE",
        "value": emailId,
        "primary": true
    }
    payload["emails"] = [];
    payload["emails"].push(email);
}

// phone numbers | if there are multiple phone numbers | rename columns as 'phone1', 'phone2' and 'phone3'

if (data["phone1"] != "") {
    var phone1 = data["phone1"];
    var phone1_obj = {
        "type": "MOBILE",
        "dialCode": "+91",
        "code": "IN",
        "value": phone1,
        "primary": true
    }

    payload["phoneNumbers"] = [];
    payload["phoneNumbers"].push(phone1_obj);

    if (data["phone2"] != "") {
        var phone2 = data["phone2"];
        var phone2_obj = {
            "type": "MOBILE",
            "dialCode": "+91",
            "code": "IN",
            "value": phone2,
            "primary": false
        }
        payload["phoneNumbers"].push(phone2_obj);

        if (data["phone3"] != "") {
            var phone3 = data["phone3"];
            var phone3_obj = {
     

```json
{{body}}
```

## Kylas Notification APIs

#### Incoming Call
`POST https://api.kylas.io/v1/notifications/send-notification`

```json
{
    // Specify the type of notification, whether it's an incoming call or outgoing call.
    "notificationType": "INCOMING_CALL",
    // Define the category of the notification, such as "Others" or any relevant category.
    "category": "OTHERS", //System,Communication,Mentions,Goal,Others
    // For both incoming and outgoing calls, notifications can't be sent to all users; a specific user ID must be mentioned.
    "sendTo": {
        "user": {
            "all": false, // Set to false to notify specific users only.
            "id": [
                8112 // Example user ID
            ]
        },
        "team": {
            // Set to false to avoid sending the notification to all teams.
            "all": false,
            "id": [] // You can specify team IDs here if needed
        }
    },
    // Assign a unique remote ID to trigger the notification every time.
    "remoteId": "52120917-9967-4c0b-bb17-888fd2c3c8f4",
    // Provide a title for the notification.
    "title": " Title for incoming call Notification",
    // Add a description to provide additional context to the user receiving the notification.
    "description": "Add descroicption for user to understand",
    // Specify entities and their IDs to allow users to redirect to specific entities.
    "entities": [
        {
            "id": 218411, // Example entity ID
            "entityType": "DEAL" // Specify the type of entity (e.g., DEAL, LEAD, CONTACT)
        },
        {
            "id": 499684,
            "entityType": "LEAD"
        },
        {
            "id": 259645,
            "entityType": "CONTACT"
        }
    ],
    // Add multiple URLs with their display names to provide additional resources or links.
    "urls": [
        {
            "displayName": "Try accessing Url 1",
            "url": "https://app.kylas.io/"
        },
        {
            "displayName": "Try accessing Url 2",
            "url": "https://octavia.biz"
        }
    ],
    // Set the position of the notification popup on the user's screen. Options include: "LEFT_TOP", "LEFT_BOTTOM", "RIGHT_TOP", "RIGHT_BOTTOM".
    "position": "LEFT_BOTTOM"
}
```

#### Outgoing Call
`POST https://api.kylas.io/v1/notifications/send-notification`

```json
{
    // Specify the type of notification, whether it's an outgoing call or incoming call.
    "notificationType": "OUTGOING_CALL",
    // Define the category of the notification, such as "Others" or any relevant category.
    "category": "OTHERS", //System,Communication,Mentions,Goal,Others
    // For both incoming and outgoing calls, notifications can't be sent to all users; a specific user ID must be mentioned.
    "sendTo": {
        "user": {
            "all": false, // Set to false to notify specific users only.
            "id": [
                8112 // Example user ID
            ]
        },
        "team": {
            // Set to false to avoid sending the notification to all teams.
            "all": false,
            "id": []
        }
    },
    // Assign a unique remote ID to trigger the notification every time.
    "remoteId": "841aec3a-c0b8-4b09-9510-eecc1705dbf0",
    // Provide a title for the notification.
    "title": "Title for Outgoing Call Notification",
    // Add a description to provide additional context to the user receiving the notification.
    "description": "Customer", // Example: "Initiating a crucial client conversation"
    // Specify entities and their IDs to allow users to redirect to specific entities.
    "entities": [
        {
            "id": 218411, // Example entity ID
            "entityType": "DEAL" // Specify the type of entity (e.g., DEAL, LEAD, CONTACT)
        },
        {
            "id": 499684,
            "entityType": "LEAD"
        },
        {
            "id": 259645,
            "entityType": "CONTACT"
        }
    ],
    // Add multiple URLs with their display names to provide additional resources or links.
    "urls": [
        {
            "displayName": "Try accessing this URL 1",
            "url": "https://app.kylas.io/"
        },
        {
            "displayName": "Try accessing URL 2",
            "url": "http://harry.net"
        },
        {
            "displayName": "Try accessing URL 3",
            "url": "http://virgie.info"
        }
    ],
    // Set the position of the notification popup on the user's screen. Options include: "LEFT_TOP", "LEFT_BOTTOM", "RIGHT_TOP", "RIGHT_BOTTOM".
    "position": "RIGHT_TOP"
}
```

#### Custom
`POST https://api.kylas.io/v1/notifications/send-notification`

```json
{
    // Specify the type of notification; it is a CUSTOM type.
    "notificationType": "CUSTOM",
    // Define the category of the notification, such as "Others" or any relevant category from notifications.
    "category": "OTHERS", //System,Communication,Mentions,Goal,Others 
    // You can now send notifications to all users within the tenant.
    "sendTo": {
        "user": {
            "all": true, // Set to true to notify all users.
            "id": [] // If you want to send a notification to specific users, you can add their user IDs here with 'all' set to false.
        },
        // You can now send notifications to all teams within the tenant.
        "team": {
            "all": false, // Set to true to notify all users in all teams.
            "id": [
                113,
                114 // Example team ID
            ] // If you want to send a notification to a specific team, you can add the team ID here with 'all' set to false.
        }
    },
    // Assign a unique remote ID to trigger the notification every time.
    "remoteId": "172c6654-4f0e-4997-bf36-960b6d70b3df",
    // Provide a title for the notification.
    "title": "Quality-focused",
    "description": "Lead",
    // In custom type notifications, you can add below entities to redirect users to specific entities.
    "entities": [
        {
            "id": 218411, // Example entity ID
            "entityType": "DEAL" // Specify the type of entity (e.g., DEAL, LEAD, CONTACT)
        },
        {
            "id": 499810,
            "entityType": "LEAD"
        },
        {
            "id": 259645,
            "entityType": "CONTACT"
        },
        {
            "id": 15842,
            "entityType": "COMPANY"
        },
        {
            "id": 27036,
            "entityType": "TASK"
        },
        {
            "id": 1250,
            "entityType": "QUOTATION"
        },
        {
            "id": 9304,
            "entityType": "MEETING"
        },
        {
            "id": 60391,
            "entityType": "CALL_LOG"
        },
        {
            "id": 113416,
            "entityType": "REPORT"
        },
        {
            "id": 96951,
            "entityType": "REPORT"
        },
        {
            "id": 23007,
            "entityType": "PRODUCT"
        },
        {
            "id": 302,
            "entityType": "GOAL"
        },
        {
            "id": 8146,
            "entityType": "USER"
        },
        {
            "id": 223,
            "entityType": "TEAM"
        },
        {
            "id": 522,
            "entityType": "PROFILE"
        },
        {
            "id": 4276,
            "entityType": "WORKFLOW"
        }
    ],
    // Add multiple URLs with their display names to provide additional resources or links.
    "urls": [
        {
            "displayName": "Try accessing Url 1",
            "url": "https://app.kylas.io/"
        },
        {
            "displayName": "Try accessing Url 2",
            "url": "http://eliza.org"
        }
        // Other URLs...
    ]
}
```

## Field Sales APIs

#### Activate Executive Within Field sales 
`POST https://api.kylas.io/v1/field-sales/executives/{{EnterExecutiveID}}/activate`

#### Get Executive Timeline
`POST https://api.kylas.io/v1/field-sales/executives//{{EnterexecutiveID}}/timeline-stats`

```json
{
    "startDate": "2024-11-24T18:30:00.000Z",
    "endDate": "2024-11-25T18:29:59.999Z"
}
```

#### Get All Executive
`POST https://api.kylas.io/v1/field-sales/executives/live-location/search?page=0&size=50`

```json
{
    "fields": [],
    "jsonRule": null
}
```

#### Remove Executive
`POST https://api.kylas.io/v1/field-sales/executives/{{EnterexecutiveID}} /deactivate`

#### Get Available Executive
`POST https://api.kylas.io/v1/field-sales/executives/live-location/search?page=0&size=50`

```json
{
    "fields": [],
    "jsonRule": {
        "rules": [
            {
                "operator": "equal",
                "id": "status",
                "field": "status",
                "type": "string",
                "value": "AVAILABLE"
            }
        ],
        "condition": "AND",
        "valid": true
    }
}
```

#### Get Unavailable Executive
`POST https://api.kylas.io/v1/field-sales/executives/live-location/search?page=0&size=50`

```json
{
    "fields": [],
    "jsonRule": {
        "rules": [
            {
                "operator": "equal",
                "id": "status",
                "field": "status",
                "type": "string",
                "value": "UN_AVAILABLE"
            }
        ],
        "condition": "AND",
        "valid": true
    }
}
```

#### Get Check-In Executive
`POST https://api.kylas.io/v1/field-sales/executives/live-location/search?page=0&size=50`

```json
{
    "fields": [],
    "jsonRule": {
        "rules": [
            {
                "operator": "equal",
                "id": "status",
                "field": "status",
                "type": "string",
                "value": "CHECKED_IN"
            }
        ],
        "condition": "AND",
        "valid": true
    }
}
```

#### Add Executive
`POST https://api.kylas.io/v1/field-sales/executives`

```json
{
    "users": [
        {
            "id": {{Enter Executives ID}},
            "name": "Enter Executives Name"
        }
    ]
}
```

## Whats'App APIs

#### Get connected accounts
`GET https://api.kylas.io/v1/messages/connected-accounts`

#### Create Whats'app Template
`POST https://api.kylas.io/v1/messages/whatsapp-templates`

```json
{
    "name": "Grow Smarter, Not Harder with Kylas CRM!",
    "language": "en",
    "category": "MARKETING",
    "connectedAccount": {
        "id": {{Enter connected account id}},
        "name": "{{Enter Account Name}}",
        "businessName": "{{Enter Busineess Name}}"
    },
    "entityType": "contact",
    "components": [
        {
            "type": "BODY",
            "format": "TEXT",
            "text": " {{1}}  {{2}} \n\nGreetings from Kylas \n\nHope you are doing well , \n \nKylas CRM is here to revolutionize the way you manage your business!\n\n*   *Centralized Management:* Keep your leads, deals, and contacts organized effortlessly.\n*   *Customizable Features:* Tailor Kylas CRM to your unique business needs.\n*   *Boost Team Productivity:* Assign tasks, set goals, and track performance with ease.\n*   *Affordable for All:* Enterprise-grade features at a cost designed for growing businesses.\n\nJoin thousands of businesses already experiencing the Kylas advantage."
        },
        {
            "type": "HEADER",
            "format": "TEXT",
            "text": "All-in-One CRM for Ambitious Businesses  {{1}}"
        },
        {
            "type": "FOOTER",
            "format": "TEXT",
            "text": "Your Success, Our Mission. Kylas CRM"
        }
    ]
}
```

#### Get Variable mapping
`GET https://api.kylas.io/v1/messages/whatsapp-templates/{{Whatsa'apptemplateid}}/variable-mappings`

#### Get Entity template variables
`GET https://api.kylas.io/v1/messages/whatsapp-templates/lead/variables`

#### Save Variable Mapping For Template
`POST https://api.kylas.io/v1/messages/whatsapp-templates/{{tempalteid}}/variable-mappings/save`

```json
{
    "variableMappings": [
        {
            "id": {{Enter variable mapping id}},
            "componentType": "BODY",
            "templateVariable": 1,
            "entity": "lead",
            "internalName": "firstName",
            "fallbackValue": "User",
            "fieldType": "TEXT_FIELD"
        },
        {
            "id": {{Enter variable mapping id}},
            "componentType": "BODY",
            "templateVariable": 2,
            "entity": "lead",
            "internalName": "lastName",
            "fallbackValue": "",
            "fieldType": "TEXT_FIELD"
        }
    ]
}
```

#### Edit Whats'app Template
`PUT https://api.kylas.io/v1/messages/whatsapp-templates/{{Templateid}}`

```json
{
    "name": "Whatsapp template for API publication",
    "language": "en",
    "category": "MARKETING",
    "connectedAccount": {
        "id": 4,
         "name": "{{Enter Account Name}}",
        "businessName": "{{Enter Busineess Name}}"
    },
    "entityType": "lead",
    "components": [
        {
            "type": "BODY",
            "format": "TEXT",
            "text": "Hello  {{1}}   {{2}}  \n \nIs your business ready to take the next step in growth? With Kylas CRM, you can:  \n \n* *Simplify Sales Management:* Keep track of leads, deals, and contacts all in one place.  \n* *Leverage Data Insights:* Make informed decisions with customizable reports and dashboards.  \n* *Enhance Collaboration:* Share data securely across your team for seamless coordination.  \n* *Scale With Ease:* Designed for growing businesses, Kylas CRM adapts to your needs.  \n \nStay ahead of the competition with a CRM built to simplify your processes and maximize your results."
        },
        {
            "type": "HEADER",
            "format": "TEXT",
            "text": "Header: Empower Your Sales, Streamline Your Growth"
        },
        {
            "type": "FOOTER",
            "format": "TEXT",
            "text": "Your Partner in Growth, Kylas CRM"
        }
    ]
}
```

#### Get phone number with Session Info
`GET https://api.kylas.io/v1/messages/connected-accounts/{{Connectedaccountid}}/lead/{{leadid}}/phone-numbers`

#### Send Template message 
`POST https://api.kylas.io/v1/messages/whatsapp-templates/{{Templateid}}/send`

```json
{
    "entityId": {{ENter lead id}},
    "entityType": "lead",
    "phoneId": {{Enter Phone number id}}
}
```

#### Get Whats'app Templates  
`POST https://api.kylas.io/v1/messages/whatsapp-templates/search?sort=updatedAt,desc&page=1&size=10`

```json
{"jsonRule":null}
```

#### Send Session message
`POST https://api.kylas.io/v1/messages/connected-accounts/6/session-message`

```json
{
    "entityId": {{enter Lead or contact ID }},
    "entityType": "lead",
    "phoneId": {{eanter Phone number ID}},
    "messageType": "text",
    "messageBody": "{{Enter your message }}."
}
```

#### Send media session message
`POST https://api.kylas.io/v1/messages/connected-accounts/{{Connected account id}}/media-session-message`

#### Get Message details
`GET https://api.kylas.io/v1/conversations/{{conversation_id}}/messages/{{meesaage id}}?entityId={{lead id}}&entityType=lead`

#### Get Messages 
`POST https://api.kylas.io/v1/messages/conversations/{{conversation_id}}/search?page=1&size=10`

```json
{
    "jsonRule": {
        "rules": [
            {
                "id": "related_to",
                "field": "related_to",
                "type": "related_lookup",
                "value": {
                    "entity": "lead",
                    "id": "{{enter lead ID}}"
                },
                "operator": "equal"
            }
        ],
        "condition": "AND"
    }
}
```

#### Map UTM fields
`POST https://api.kylas.io/v1/messages/connected-accounts/5/mapped-fields/lead`

```json
{
    "campaign": 442971,
    "source": 442972,
    "subSource": "{{Enter Sub Source}}",
    "utmCampaign": "{{Enter UTM Campaign}}",
    "utmContent": "{{Enter UTM Content}}",
    "utmMedium": "{{ Enter UTM Medium}}",
    "utmSource": "{{Enter UTM Source}}",
    "utmTerm": "{{Enter UTM Term }}"
}
```

#### Get  Whats'app credit Usage 
`POST https://api.kylas.io/v1/messages/whatsapp-credits/history?page=1&size=10`

```json
{
    "jsonRule": {
        "condition": "AND",
        "rules": [
            {
                "id": "startTime",
                "field": "startTime",
                "type": "date",
                "operator": "today",
                "value": null,
                "timeZone": "Asia/Calcutta"
            }
        ],
        "valid": true
    }
}
```

## Shifts

#### Create Shift
`POST https://api.kylas.io/v1/shifts`

```json
{
    "name": "{{Enter SHift Name}}",
    "timezone": "Asia/Calcutta",
    "recordAssignment": [
        {
            "day": "MONDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "TUESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "WEDNESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "THURSDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "FRIDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SATURDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 0,
                    "startMinute": 0,
                    "endHour": 23,
                    "endMinute": 59
                }
            ]
        },
        {
            "day": "SUNDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 0,
                    "startMinute": 0,
                    "endHour": 23,
                    "endMinute": 59
                }
            ]
        }
    ],
    "calling": [
        {
            "day": "MONDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "TUESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "WEDNESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "THURSDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "FRIDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SATURDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SUNDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        }
    ],
    "messaging": [
        {
            "day": "MONDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "TUESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "WEDNESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "THURSDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "FRIDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SATURDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SUNDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        }
    ]
}
```

#### Edit Shift
`PUT https://api.kylas.io/v1/shifts/17578`

```json
{
    "id": {{Enter Shift id}},
    "name": "{{ENter Shift Name}}",
    "timezone": "Asia/Calcutta",
    "createdAt": "2024-11-28T10:16:35.709Z",
    "updatedAt": "2024-11-28T10:16:35.709Z",
    "createdBy": {
        "id": {{ENter USer ID}},
        "name": "{{Enter user Name}}"
    },
    "updatedBy": {
        "id": {{ENter USer ID}},
        "name": "{{Enter user Name}}"
    },
    "recordActions": {
        "read": true,
        "write": true,
        "update": true,
        "delete": true,
        "email": false,
        "call": false,
        "sms": false,
        "task": false,
        "note": false,
        "meeting": false,
        "document": false,
        "readAll": true,
        "updateAll": true,
        "deleteAll": true,
        "quotation": false,
        "reshare": false,
        "reassign": false
    },
    "assignedUsers": 0,
    "recordAssignment": [
        {
            "day": "MONDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "TUESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "WEDNESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "THURSDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "FRIDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SATURDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 0,
                    "startMinute": 0,
                    "endHour": 23,
                    "endMinute": 59
                }
            ]
        },
        {
            "day": "SUNDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 0,
                    "startMinute": 0,
                    "endHour": 23,
                    "endMinute": 59
                }
            ]
        }
    ],
    "calling": [
        {
            "day": "MONDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "TUESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "WEDNESDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "THURSDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "FRIDAY",
            "available": true,
            "slot": [
                {
                    "id": null,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": null,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SATURDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SUNDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        }
    ],
    "messaging": [
        {
            "day": "MONDAY",
            "available": true,
            "slot": [
                {
                    "id": 367718,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": 367719,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": 367720,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "TUESDAY",
            "available": true,
            "slot": [
                {
                    "id": 367721,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": 367722,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": 367723,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "WEDNESDAY",
            "available": true,
            "slot": [
                {
                    "id": 367724,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": 367725,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": 367726,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "THURSDAY",
            "available": true,
            "slot": [
                {
                    "id": 367727,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": 367728,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": 367729,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "FRIDAY",
            "available": true,
            "slot": [
                {
                    "id": 367730,
                    "startHour": 10,
                    "startMinute": 0,
                    "endHour": 13,
                    "endMinute": 0
                },
                {
                    "id": 367731,
                    "startHour": 14,
                    "startMinute": 0,
                    "endHour": 16,
                    "endMinute": 0
                },
                {
                    "id": 367732,
                    "startHour": 16,
                    "startMinute": 15,
                    "endHour": 19,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SATURDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        },
        {
            "day": "SUNDAY",
            "available": false,
            "slot": [
                {
                    "id": null,
                    "startHour": 9,
                    "startMinute": 0,
                    "endHour": 18,
                    "endMinute": 0
                }
            ]
        }
    ]
}
```

#### Get Shifts
`POST https://api.kylas.io/v1/shifts/search?sort=updatedAt,desc&page=0&size=10`

```json
{
    "fields": [],
    "jsonRule": null
}
```

## Score Rule

#### Create Score Rule
`POST https://api.kylas.io/v1/score-rules`

```json
{
    "name": "{{Enter the RUle Name }}",
    "ruleField": {
        "id": "score",
        "name": "Score",
        "standard": true
    },
    "active": true,
    "ruleType": "POSITIVE",
    "entityType": "LEAD",
    "criteria": [
        {
            "event": "LEAD",
            "condition": {
                "conditionType": "CONDITION_BASED",
                "conditions": [
                    {
                        "name": "firstName",
                        "value": "{{Enter the value of field}}",
                        "operator": "equal",
                        "fieldType": "TEXT_FIELD",
                        "standard": true
                    },
                    {
                        "operator": "and"
                    },
                    {
                        "name": "ownerId",
                        "value": {
                            "id": {{Enter User ID}},
                            "name": "{{Enter user Name}}"
                        },
                        "operator": "equal",
                        "fieldType": "LOOK_UP",
                        "standard": true
                    },
                    {
                        "operator": "and"
                    },
                    {
                        "name": "pipelineStage",
                        "value": {
                            "id": {{Enter pipeline Id}},
                            "name": "Default Lead Pipeline",
                            "stage": {
                                "id": {{Enter Pipeline stage ID}},
                                "name": "Open"
                            }
                        },
                        "operator": "equal",
                        "fieldType": "PIPELINE_STAGE",
                        "standard": true
                    }
                ]
            },
            "scoreValue": 1
        },
        {
            "event": "LEAD",
            "condition": {
                "conditionType": "CONDITION_BASED",
                "conditions": [
                    {
                        "name": "city",
                        "value": "{{Enter the field value}}",
                        "operator": "equal",
                        "fieldType": "TEXT_FIELD",
                        "standard": true
                    },
                    {
                        "operator": "or"
                    },
                    {
                        "name": "companyCity",
                        "value": "{{enter field Value}}",
                        "operator": "equal",
                        "fieldType": "TEXT_FIELD",
                        "standard": true
                    }
                ]
            },
            "scoreValue": 1
        }
    ]
}
```

#### Get Score  Rules
`POST https://api.kylas.io/v1/score-rules/search/lead?page=0&size=10&sort=updatedAt,desc`

```json
{
    "fields": [
        "name",
        "ruleType",
        "ruleField",
        "updatedAt",
        "active",
        "numberOfCriteria",
        "triggerCount",
        "lastTriggeredAt"
    ],
    "jsonRules": null
}
```

#### Get Score Rule Details
`GET https://api-qa.sling-dev.com/v1/score-rules/{{Add Score Rule ID}}`

#### Deactivate Score Rule
`POST https://api.kylas.io/v1/score-rules/{{ENter Score Rule ID}}/deactivate`

#### Activate Score Rule
`POST https://api.kylas.io/v1/score-rules/{{ENter Score Rule ID}}/activate`

#### Update Score Rule
`PUT https://api.kylas.io/v1/score-rules/{{Add Score Rule ID}}`

```json
{
    "id": 51,
    "tenantId": 4374,
    "name": "{{Enter the RUle Name }}",
    "ruleType": "POSITIVE",
    "entityType": "LEAD",
    "ruleField": {
        "id": "score",
        "name": "Score",
        "standard": true
    },
    "triggerCount": 0,
    "active": false,
    "criteria": [
        {
            "id": 86,
            "event": "LEAD",
            "condition": {
                "conditionType": "CONDITION_BASED",
                "conditions": [
                    {
                        "operator": "equal",
                        "name": "pipelineStage",
                        "value": {
                            "id": 7540,
                            "name": "Deployement",
                            "stage": {
                                "id": 47072,
                                "name": "Artifact Creation "
                            },
                            "stages": null,
                            "pipelineStageReason": null
                        },
                        "standard": true
                    }
                ]
            },
            "scoreValue": 20
        },
        {
            "event": "LEAD",
            "condition": {
                "conditionType": "CONDITION_BASED",
                "conditions": [
                    {
                        "name": "ownerId",
                        "value": {
                            "id": 11214,
                            "name": "Britanney Raymond"
                        },
                        "operator": "equal",
                        "fieldType": "LOOK_UP",
                        "standard": true
                    }
                ]
            },
            "scoreValue": 10
        }
    ],
    "createdBy": {
        "id": 11213,
        "name": "Score Edit"
    },
    "updatedBy": {
        "id": 11213,
        "name": "Score Edit"
    },
    "createdAt": "2025-01-13T10:31:58Z",
    "updatedAt": "2025-01-13T10:47:37Z",
    "lastTriggeredAt": null,
    "recordActions": {
        "read": true,
        "update": true,
        "write": true,
        "readAll": false,
        "updateAll": false,
        "email": false,
        "call": false,
        "sms": false,
        "task": false,
        "note": false,
        "meeting": false,
        "document": false
    }
}
```

#### Colour Range configuration
`PUT https://api.kylas.io/v1/score-rules/color-configuration/lead`

```json
[
    {
        "from": 0,
        "to": 10,
        "hexCode": "#DA2D1F"
    },
    {
        "from": 10,
        "to": 20,
        "hexCode": "#F57273"
    },
    {
        "from": 20,
        "to": 30,
        "hexCode": "#FFA500"
    },
    {
        "from": 30,
        "to": 40,
        "hexCode": "#F57273"
    },
    {
        "from": 40,
        "to": 50,
        "hexCode": "#F57273"
    },
    {
        "from": 50,
        "to": 60,
        "hexCode": "#7856FF"
    },
    {
        "from": 60,
        "to": 70,
        "hexCode": "#006DEE"
    },
    {
        "from": 70,
        "to": 80,
        "hexCode": "#7856FF"
    },
    {
        "from": 80,
        "to": 90,
        "hexCode": "#B4FD75"
    },
    {
        "from": 90,
        "to": 100,
        "hexCode": "#52A351"
    }
]
```

