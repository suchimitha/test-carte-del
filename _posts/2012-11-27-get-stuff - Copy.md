---
category: Contact Operations
title: 'Create Xero Contact'

layout: nil
---

This method allows users to retrieve Invoice Operations.

### Request

* The headers must include a **valid authentication token**.

### Response

Sends back a collection of things.

```Status: 200 OK```
```{
    {
        id: thing_1,
        name: 'My first thing'
    },
    {
        id: thing_2,
        name: 'My second thing'
    }
}```

For errors responses, see the [response status codes documentation](#response-status-codes).