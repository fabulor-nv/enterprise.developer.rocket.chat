# Register a new Livechat visitor

| URL                        | Requires Auth | HTTP Method |
| -------------------------- | ------------- | ----------- |
| `/api/v1/livechat/visitor` | `no`          | `POST`      |

## Example payload

```javascript
{
  "visitor": {
    "name": "Livechat Visitor",
    "email": "visitor@rocket.chat",
    "token": "iNKE8a6k6cjbqWhWd",
    "phone": "55 51 5555-5555",
    "customFields": [{
      "key": "address",
      "value": "Rocket.Chat street",
      "overwrite": true
    }]
  }
}
```

## Example Call

```bash
curl -X POST \
     -H "Content-type:application/json" \
     http://localhost:3000/api/v1/livechat/visitor \
    -d '{"visitor": {"name": "Livechat Visitor", "email": "visitor@rocket.chat", "token": "iNKE8a6k6cjbqWhWd", "phone": "55 51 5555-5555", "customFields": [{ "key": "address", "value": "Rocket.Chat street", "overwrite": true }] }}'
```

## Example Result

```javascript
{
  "visitor": {
    "_id": "sGtcfEYz852uguxaS",
    "username": "guest-7",
    "_updatedAt": "2018-09-21T16:12:32.808Z",
    "token": "iNKE8a6k6cjbqWhWd",
    "phone": [
      {
        "phoneNumber": "55 51 5555-5555"
      }
    ],
    "visitorEmails": [
      {
        "address": "visitor@rocket.chat"
      }
    ],
    "name": "Livechat Visitor",
    "livechatData": {
      "address": "Rocket.Chat street"
    }
  },
  "success": true
}
```
