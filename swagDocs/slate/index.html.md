---
title: API Reference

language_tabs:
  - shell
  - ruby
  - python

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

* Documentation: https://apideveloper.vantiv.com/docs/devhub-developer
* Forum: https://apideveloper.vantiv.com/forum
* FAQ: https://apideveloper.vantiv.com/faqs

# Authentication

* DevHub Account (https://apideveloper.vantiv.com)
* License from DevHub Account

Devhub uses API keys to allow access to the API. You can register a new API key at our [developer portal](https://apideveloper.vantiv.com).

Devhub expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: VANTIV license="{{License}}`

<aside class="notice">
You must replace <code>License</code> with your personal API key.
</aside>

# Account

## Delete an account

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "https://apis.cert.vantiv.com/v1/account"
  -H "Authorization: License"
  -d "
  {
  "Application": {
    "ApplicationID": "string",
    "ApplicationName": "string",
    "ApplicationVersion": "string"
  },
  "PaymentAccount": "string"
}"
```

> The above command returns JSON structured like this:

```json
[
  {
    "ExpressResponseCode": "string",
    "ExpressResponseMessage": "string",
    "ExpressTransactionDate": "string",
    "ExpressTransactionTime": "string",
    "ExpressTransactionTimezone": "string",
    "PaymentAccount": {
      "PaymentAccountID": "string",
      "PaymentAccountReferenceNumber": "string"
    },
    "ServicesID": "string"
  }
]
```

This endpoint deletes an account.

### HTTP Request

`DELETE https://apis.cert.vantiv.com/v1/account`

### Parameters

Parameter | Description
--------- | -----------
Content-Type | Description of Content-Type
Accept | Description of Accept
Authorization | Your personal API key

### Body
Parameter | Description
--------- | -----------
Application | Consists of ApplicationID, ApplicationName, ApplicationVersion
PaymentAccount | String

### Application
Parameter | Description
--------- | -----------
ApplicationID | String
ApplicationName | String
ApplicationVersion | String 

<aside class="success">
Remember — You must replace <code>License</code> with your personal API key.
</aside>

## Post to an account

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl -X POST 
--header 'Content-Type: application/json' 
--header 'Accept: application/json' 
-d "{
  "Application": {
    "ApplicationID": "string",
    "ApplicationName": "string",
    "ApplicationVersion": "string"
  },
  "PaymentAccount": "string",
  "Card": {
    "Track1Data": "string",
    "Track2Data": "string",
    "MagneprintData": "string",
    "EncryptedTrack1Data": "string",
    "EncryptedTrack2Data": "string",
    "EncryptedCardData": "string",
    "CardDataKeySerialNumber": "string",
    "EncryptedFormat": "Default",
    "CardNumber": "string",
    "ExpirationMonth": "string",
    "ExpirationYear": "string"
  },
  "DemandDepositAccount": {
    "AccountNumber": "string",
    "RoutingNumber": "string"
  },
  "Address": {
    "BillingName": "string",
    "BillingAddress1": "string",
    "BillingAddress2": "string",
    "BillingCity": "string",
    "BillingState": "string",
    "BillingZipcode": "string",
    "BillingEmail": "string",
    "BillingPhone": "string",
    "ShippingName": "string",
    "ShippingAddress1": "string",
    "ShippingAddress2": "string",
    "ShippingCity": "string",
    "ShippingState": "string",
    "ShippingZipcode": "string",
    "ShippingEmail": "string",
    "ShippingPhone": "string"
  }
}""
```

> The above command returns JSON structured like this:

```json
[
  {
    "ExpressResponseCode": "string",
    "ExpressResponseMessage": "string",
    "ExpressTransactionDate": "string",
    "ExpressTransactionTime": "string",
    "ExpressTransactionTimezone": "string",
    "PaymentAccount": {
      "PaymentAccountID": "string",
      "PaymentAccountReferenceNumber": "string"
    },
    "ServicesID": "string"
  }
]
```

This endpoint posts to an account.

### HTTP Request

`POST https://apis.cert.vantiv.com/v1/account`

### Headers

Parameter | Description
--------- | -----------
Content-Type | Description of Content-Type
Accept | Description of Accept
Authorization | Your personal API key

### Body
Parameter | Contents
--------- | -----------
Application | Consists of ApplicationID, ApplicationName, ApplicationVersion
PaymentAccount | String
Card |  Track1Data, Track2Data, MagneprintData, EncryptedTrack1Data, EncryptedTrack2Data, EncryptedCardData, CardDataKeySerialNumber, EncryptedFormat: Default, CardNumber, ExpirationMonth, ExpirationYear
DemandDepositAccount | AccountNumber,RoutingNumber
Address | BillingName, BillingAddress1, BillingAddress2, BillingCity, BillingState, BillingZipcode, BillingEmail, BillingPhone, ShippingName, ShippingAddress1,ShippingAddress2, ShippingCity, ShippingState, ShippingZipcode, ShippingEmail, ShippingPhone


#### Application
Parameter | Data Type
--------- | -----------
ApplicationID | String
ApplicationName | String
ApplicationVersion | String 

#### Card
Parameter | Data Type
--------- | -----------
Track1Data | string
Track2Data | string
MagneprintData | string
EncryptedTrack1Data | string
EncryptedTrack2Data | string
EncryptedCardData | string
CardDataKeySerialNumber | string
EncryptedFormat | Default
CardNumber | string
ExpirationMonth | string
ExpirationYear | string

#### DemandDepositAccount
Parameter | Description
--------- | -----------
AccountNumber | string
RoutingNumber | string

#### Address
Parameter | Description
--------- | -----------
BillingName | string
BillingAddress1 | string
BillingAddress2 | string
BillingCity | string
BillingState | string
BillingZipcode | string
BillingEmail | string
BillingPhone | string
ShippingName | string
ShippingAddress1 | string
ShippingAddress2 | string
ShippingCity | string
ShippingState | string
ShippingZipcode | string
ShippingEmail | string
ShippingPhone | string

<aside class="success">
Remember — You must replace <code>License</code> with your personal API key.
</aside>

