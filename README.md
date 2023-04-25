# Games API Docs
This API is used to consume a json of games available on the Games Store
## Endpoints
### GET / games
This endpoint is responsible for returning the entire list of games registered in the database
#### Parameters
None
#### Responses
##### OK! 200
If the response happens you will receive the list of games.  

**Example:**
```

[
    {
        "id": 2,
        "title": "Mortal Kombat",
        "year": 2019,
        "price": 10
    },
    {
        "id": 3,
        "title": "Harry Potter Legacy",
        "year": "2023",
        "price": "70"
    },
    {
        "id": 4,
        "title": "It Takes Two",
        "year": "2020",
        "price": "40"
    }
]

```
##### Unauthorized! 401
If this response happens, it means that there was an authentication failure in the request. _Reasons:_ invalid token, inspired token.  

**Example:**
```

{
    "err": "Falhou!"
}

```


## Endpoints
### POST / auth
This endpoint is responsible for logging into the API
#### Parameters

_Email_: email registered in the system.  
_Password_: password registered in the system.  

**Example:**  
```

{
    "email": "example@email.com",
    "password": "****"
}

```
#### Responses
##### OK! 200
If the response happens you will receive the JWT token to access protected endpoints in the API  

**Example:**
```

{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NTY0LCJlbWFpbCI6ImluZ3JpZGdpYW55QGdtYWlsLmNvbSIsImlhdCI6MTY4MjQxNzE0NSwiZXhwIjoxNjgyNDUzMTQ1fQ.v2xI02-jqLje9nNhANnFcyj9pFR4Qj808rzbMprSK6g"
}

```
##### Unauthorized! 401
If this response happens, it means that there was an authentication failure in the request. _Reasons:_ invalid email, invalid password.  

**Example:**
```

{ 
err: 'Unauthorized' 
}

```



















