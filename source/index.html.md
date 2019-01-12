---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://lovely-ads.com'>LovelyAds (Website)</a>
  - <a href='https://app.lovely-ads.com'>LovelyAds (App)</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the LovelyAds API!

# Authentication

> To authorize, use this code:

```shell
  curl --request POST \
    --url https://api.lovely-ads.com/auth/login \
    --header 'content-type: application/json' \
    --data '{
    "email": "john.doe@example.com",
    "password": "123456"
  }'
```
> The above command returns JSON structured like this:

```json
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.(...).hfrE13-waIs2G05zx1GInF_CVJAfJxD52R9QNoVDwDA",
  "id": "1f2dd3b0-cd56-11e8-8bdb-e7a88219db52",
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com",
  "avatar": null,
  "newUser": false,
  "role": 2
}
```
> The presented key is false and shortened.


```shell
curl "api_endpoint_here"
  -H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9..."
```

LovelyAds uses JWT (Json Web Tokens) for authentication.

First you need to login by sending your email and password. If the given values are correct you'll receive a message with the token to be used as well as the user's informations.

The token needs to be used in the *Authorization* header field using the *Bearer* prefix.

# Kittens

## Get All Kittens

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

# AdGroups

## List all AdGroups

## Update AdGroup



# Billing

## List all Billing

## Create a Credit Card

## Create a SEPA



# Campaigns

## Update a Campaign



# Catalogs

## List all Catalogs

## Retrieve Stats



# Companies

## Retrieve a Company

## Create Company

## Update a Company

## List all Companies

## List all Users for a Company

## List all Websites for a Company

## List all Invoices for a Company

## List all Billing for a Company

## Update a Billing for a Company

## Delete a Billing for a Company

## Update Permissions for a Company

## Attach a Company

## Detach a Company



# Keywords


# Opportunities


# Plans


# Products


# Providers


# Rules


# Structures


# Terms


# Users


# Validations


# Websites
