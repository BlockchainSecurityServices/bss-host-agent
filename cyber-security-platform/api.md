---
description: Cyber Security Platform API
---

# API

{% api-method method="get" host="https://api.blockchainsecurity.services" path="/v1/assets/" %}
{% api-method-summary %}
Get Assets
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token required for access control.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Asset successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "assetName": "Asset name",
    "assetSummary": "Summary name",
    "assetType": "Web Server",
    "assetCategory": "Web App",
    "assetValue": "high",
    "status": "Vulnerable",
    "lastScanedOn" : "01/01/19"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find an ass matching this query.
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



