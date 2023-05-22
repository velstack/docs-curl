<p align="center"><a href="https://mnotify.com" target="_blank"><img src="https://dashboard.velstack.com/public/assets/images/velstack/logo-white.png" width="200" alt="  Logo"></a></p>

<p align="center">
<a href="https://github.com/sammyfort/mNotify-laravel"><img src="https://img.shields.io/badge/%3C%2F%3E-cURL%20-blue" alt="Build Status"></a>
<a href="https://packagist.org/packages/velstack/mnotify"><img src="https://img.shields.io/github/license/sammyfort/mNotify-laravel"></a>

 

</p>
 

## Velstack [cURL] documenation.

## Introduction
Velstack APIs was made with REST and uses http verbs such as `'GET'`, `'POST'`, `'PATCH/PUT'`, `'DELETE'`. Every request to our endpoints must be restful.

Base url
```bash
  https://api.velstack.com
```

## Authentication

Velstack uses API keys to `'authenticate'` requests. You can [register](https://dashboard.velstack.com/) or login to get yur API key.
Eevery request made to this endpoint requires API key to the server as a GET parameter:.   

## Responses

All http responses are in json format that's every request to our endpoint must include a header of `'Accept:application/json'` .   

 
## Send Quick SMS

```shell
curl https://api.velstack.com/messaging/quick/sms
-H "Authorization: Bearer YOUR_API_KEY"
-H "Accept: application/json"
-d '{ "sender" : "Velstack", recipient: "020XXXX9304", message: "First sms with velstack Apis" }'
-X POST

```
 
 
 
 

#### `Response`
```json
{
       "status": true,
    "code": 200,
    "message": "Message sent successfully",
    "data": {
        "summary": {
            "message_id": "3934ac17-25e8-46cb-ac27-4963b78f87ee",
            "type": "API Quick SMS",
            "total_contacts": 1,
            "recipients": "0205550368",
            "credit_used": 1,
            "credit_left": "0.00"
        }
    }
}

```
 
  
<p align="center">
  Sammy Fort ©2023. Powered by <a href="https://velstack.com/">Velstack</a>
</p>
