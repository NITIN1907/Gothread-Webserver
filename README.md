# Go Thread-Safe User API

A minimal RESTful API built in Go to manage user data using an in-memory cache. The server is designed with concurrency in mind, utilizing `sync.RWMutex` to ensure thread-safe operations when accessing or modifying the shared `userCache`.

## 🚀 Features

- Create a new user (POST `/users`)
- Retrieve user by ID (GET `/users/{id}`)
- Delete user by ID (DELETE `/users/{id}`)
- In-memory data store (no database)
- Thread-safe implementation using `sync.RWMutex`

## 🧠 Technologies Used

- Go (Golang)
- `net/http`
- `sync` package for thread safety
- JSON for request and response encoding

## 📦 Endpoints

### `GET /`

- Returns: `"hello world"`

### `POST /users`

- Request Body:

```json
{
  "name": "John Doe"
}
