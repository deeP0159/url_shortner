# 🧩 Go URL Shortener

A simple and lightweight URL shortener built with **Go (Golang)**.  
It takes long URLs and converts them into short, unique hashes using the **MD5 algorithm**.  
Includes REST endpoints to shorten URLs and redirect users to the original links.

---

## 🚀 Features
- 🔗 Shorten any valid URL via a simple JSON POST request  
- ↪️ Redirect to the original URL using the generated short code  
- 🧠 In-memory storage for quick testing and development  
- 🧰 Clean, minimal REST API built with Go’s standard `net/http` package  
- ⏰ Automatically records creation time for each shortened link  

---

## ⚙️ Endpoints

| Method | Endpoint | Description |
|--------|-----------|-------------|
| `GET`  | `/`              | Welcome page |
| `POST` | `/shorten`       | Shortens a long URL |
| `GET`  | `/redirect/{id}` | Redirects to the original URL |

---

## 🧠 Example

### Create a short URL
```bash
curl -X POST http://localhost:3000/shorten \
  -H "Content-Type: application/json" \
  -d '{"url": "https://github.com"}'
