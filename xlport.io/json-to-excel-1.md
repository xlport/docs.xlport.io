# JSON to Excel

{% api-method method="put" host="https://xlport.compute.molnify.com" path="/export" %}
{% api-method-summary %}
export
{% endapi-method-summary %}

{% api-method-description %}
Convert arbitrary JSON to custom Excel template. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Authorization token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="filename" type="string" required=false %}
output filename, default value "Result"
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="object" required=false %}
JSON data
{% endapi-method-parameter %}

{% api-method-parameter name="templateId" type="string" required=true %}
filename of the pre-uploaded Excel template
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}





