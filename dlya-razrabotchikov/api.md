# API

Используйте наше API для интегрирования в свои сервисы 😉&#x20;

{% swagger method="get" path="/getInfoByEmoji" baseUrl="https://api.ton.ink/api/v1" summary="Get user info by emoji" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="emoji" required="true" type="String" %}
Emoji you want to find
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Always is okay" %}
```javascript
{
    "status": "ok",
    "data": {
        "owner": String, // владелец NFT
        "name": String, // установленное пользователем имя
        "description": String, // установленное пользователем описание
        "verified": Boolean, // галочка, выдаётся только известным людям
        "links": [
            {
                "displayName": String, // имя соц.сети/домен сайта
                "url": String // ссылка
            }
        ]
    }
}
```
{% endswagger-response %}
{% endswagger %}
