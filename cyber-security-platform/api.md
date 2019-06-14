---
description: Cyber Security Platform API
---

# API

{% api-method method="post" host="https://api.blockchainsecurity.services" path="/v1/assets/" %}
{% api-method-summary %}
Add Asset
{% endapi-method-summary %}

{% api-method-description %}
This api endpoint allows you to programmatically add an asset
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorisation" type="string" required=true %}
\(api-key:api-secret\)base64
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="Asset" type="object" required=true %}
JSON object representing an asset { asset }
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Asset successfully added .
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Asset successfully added"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find an asset matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no asset like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="https://api.blockchainsecurity.services" path="/v1/assets/:assetid" %}
{% api-method-summary %}
Update Asset
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="assetId" type="string" required=false %}
Pass assetId for asset that you intend to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="Asset" type="object" required=false %}
JSON object representing the asset {}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "Asset Updated"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "Unable to update asset"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.blockchainsecurity.services" path="/v1/assets/" %}
{% api-method-summary %}
Get Assets
{% endapi-method-summary %}

{% api-method-description %}
This api endpoint allows you get a list of one or more assets
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Authorisation" type="string" required=true %}
\(api-key:api-secret\)base64
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
A list of 1 or more Assets represented as json objects 
{% endapi-method-response-example-description %}

```
[
    {
        "assetId": {'assetName': 'My Main Asset', ...}
    },
    {
         "assetIdN": {'assetName': 'My Second Main Asset', ...}
    }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "No Assets, please add an asset"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.blockchainsecurity.services" path="/v1/assets/:assetId" %}
{% api-method-summary %}
Get Asset 
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="assetId" type="string" required=true %}
Pass assetId for asset details
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorisation" type="string" required=true %}
\(api-key:api-secret\)base4
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
A json representation of the asset is returned
{% endapi-method-response-example-description %}

```
{
    "assetName": "My Main Asset",
    "assetSummary": "",
    ...
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "No asset found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

