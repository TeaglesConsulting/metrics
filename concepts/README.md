
### Events
An event is structured rather simply, consisting of 3 key pieces of data.

1. The application that sent the event.
  - App is generated automatically based on API key sent with the request.
2. The type of event that was sent (e.g. page view, add to cart, checkout, etc.)
  - Event type is generated automatically based on URL event was sent to.
3. The data that the event consists of.
  - Data a free form data structure, accepting any valid json for storage of event data.

    curl metrics.teagles.io/v1/events/page_views -H 'Authorization : token <token>' -d '{"page" : "/products/32", "user" : {"id" : "3kj8sg1q9x", "email" : "example@example.com"} }'
Creates this event structure
```
{
  "app": {
    "id": "9283eh8d4x29h",
    "name": "ExampleApp"
  },
  "event_type": "page_views",
  "data": {
    "page": "/products/32",
    "user": {
        "id": "3kj8sg1q9x",
        "email": "example@example.com"
    }
  }
}
```
