---
title: Example Usage
deprecated: false
hidden: false
metadata:
  robots: noindex
---
:blue_heart:

Here's a **Markdown-based API usage guide** for a **Pet Store API**. This guide is written in a developer-friendly format with example requests and responses using typical RESTful API patterns. You can adapt this for your actual API endpoints, authentication methods, and response formats.

***

# 🐾 PAI Pet Store API – Usage Guide

Welcome to the **PAI Pet Store API**! This guide shows how to access pet-related data and manage store resources via our RESTful API.

***

## 🔐 Authentication

Use the API key in the request header:

```
Authorization: Bearer YOUR_API_KEY
```

***

## 📚 Endpoints

### 🔍 Get All Pets

**GET** `/api/pets`

**Request:**

```http
GET /api/pets
Authorization: Bearer YOUR_API_KEY
```

**Response:**

```json
[
  {
    "id": "1",
    "name": "Buddy",
    "type": "Dog",
    "breed": "Golden Retriever",
    "age": 3,
    "available": true
  },
  {
    "id": "2",
    "name": "Whiskers",
    "type": "Cat",
    "breed": "Siamese",
    "age": 2,
    "available": false
  }
]
```

***

### 📄 Get Pet by ID

**GET** `/api/pets/{id}`

**Example:**

```http
GET /api/pets/1
Authorization: Bearer YOUR_API_KEY
```

**Response:**

```json
{
  "id": "1",
  "name": "Buddy",
  "type": "Dog",
  "breed": "Golden Retriever",
  "age": 3,
  "available": true,
  "description": "Friendly and energetic dog, great with kids."
}
```

***

### ➕ Add a New Pet

**POST** `/api/pets`

**Request:**

```http
POST /api/pets
Content-Type: application/json
Authorization: Bearer YOUR_API_KEY

{
  "name": "Bella",
  "type": "Dog",
  "breed": "Beagle",
  "age": 1,
  "available": true
}
```

**Response:**

```json
{
  "message": "Pet added successfully",
  "id": "3"
}
```

***

### ✏️ Update Pet Info

**PUT** `/api/pets/{id}`

**Example:**

```http
PUT /api/pets/3
Content-Type: application/json
Authorization: Bearer YOUR_API_KEY

{
  "available": false
}
```

**Response:**

```json
{
  "message": "Pet updated successfully"
}
```

***

### ❌ Delete a Pet

**DELETE** `/api/pets/{id}`

```http
DELETE /api/pets/3
Authorization: Bearer YOUR_API_KEY
```

**Response:**

```json
{
  "message": "Pet deleted successfully"
}
```

***

## ⚠️ Errors

Standard error responses follow this format:

```json
{
  "error": "Unauthorized",
  "message": "Invalid API key"
}
```

***

## 📫 Support

* 📧 Email: [devsupport@paipets.com](mailto:devsupport@paipets.com)
* 🔗 Docs: [https://api.paipets.com/docs](https://api.paipets.com/docs)

***

Would you like me to generate a Postman collection or OpenAPI (Swagger) spec for this API?

![This won't be fun to clean up...](https://owlbert.io/images/popper.gif)