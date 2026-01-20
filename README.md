# 🎬 Go Movie REST API

A simple **RESTful API built with Golang** using **Gorilla Mux**.  
This project demonstrates **CRUD operations** (Create, Read, Update, Delete) on a movie resource using in-memory storage.

---

## 🚀 Features

- Built with **Go (Golang)**
- Uses **Gorilla Mux** for routing
- RESTful API design
- JSON request & response
- CRUD operations:
  - Get all movies
  - Get a single movie
  - Create a movie
  - Update a movie
  - Delete a movie

---

## 🛠 Tech Stack

- **Language:** Go
- **Router:** Gorilla Mux
- **Protocol:** HTTP
- **Data Format:** JSON

---

## 📁 Project Structure

```

.
├── main.go
├── go.mod
└── .gitignore

````

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/go-crud.git
cd go-movie-api
````

---

### 2️⃣ Initialize Go modules (if not already)

```bash
go mod init go-crud
go mod tidy
```

---

### 3️⃣ Run the server

```bash
go run main.go
```

Server will start at:

```
http://localhost:8000
```

---

## 📌 API Endpoints

### 🔹 Get all movies

```
GET /movies
```

---

### 🔹 Get movie by ID

```
GET /movies/{id}
```

Example:

```
GET /movies/1
```

---

### 🔹 Create a movie

```
POST /movies
```

**Request Body (JSON):**

```json
{
  "isbn": "12345",
  "title": "New Movie",
  "director": {
    "firstname": "John",
    "lastname": "Doe"
  }
}
```

---

### 🔹 Update a movie

```
PUT /movies/{id}
```

Example:

```
PUT /movies/1
```

**Request Body (JSON):**

```json
{
  "isbn": "54321",
  "title": "Updated Movie",
  "director": {
    "firstname": "Jane",
    "lastname": "Doe"
  }
}
```

---

### 🔹 Delete a movie

```
DELETE /movies/{id}
```

Example:

```
DELETE /movies/1
```

---

## 🧪 Testing with curl

### Get all movies

```bash
curl http://localhost:8000/movies
```

### Create a movie

```bash
curl -X POST http://localhost:8000/movies \
-H "Content-Type: application/json" \
-d '{"isbn":"111","title":"Test Movie","director":{"firstname":"A","lastname":"B"}}'
```

---

## ⚠️ Notes

* Data is stored **in-memory**, not in a database
* Data resets when the server restarts
* This project is for **learning purposes**

---

## 📚 Learning Outcomes

* Go structs and slices
* HTTP handlers in Go
* REST API concepts
* JSON encoding/decoding
* URL parameters with Gorilla Mux

---

## 🔮 Future Improvements

* Add database (MongoDB / PostgreSQL)
* Input validation
* Error handling
* Authentication (JWT)
* Docker support

---

