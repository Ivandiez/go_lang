To run this simple server: 
```
$ go run .
```

REST API Endpoints in this app:
```
/albums
 - GET - Get list of all albums, returned as JSON.
 - POST - Add a new album from request data sent as JSON.
```

```
/albums/:id
 - GET - Get an album from request data sent as JSON
```

You can check the endpoints by those queries:
```
$ curl http://localhost:8080/albums

$ curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'

$ curl http://localhost:8080/albums/2
```