# 📦 Product API (Express + MongoDB)

A simple RESTful API for managing products using **Node.js**, **Express**, and **MongoDB (Mongoose)**.

---

## ✨ Features
- ➕ Create a new product  
- 📖 Read all products  
- 🔍 Read product by ID  
- ✏️ Update product by ID  
- 🗑️ Delete product by ID  

---

## 🛠 Tech Stack
- [Node.js](https://nodejs.org/)  
- [Express](https://expressjs.com/)  
- [MongoDB](https://www.mongodb.com/)  
- [Mongoose](https://mongoosejs.com/)  
- [Body-Parser](https://www.npmjs.com/package/body-parser)  

---

## ⚙️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/product-api.git
cd product-api
```

### 2. Install dependencies
```bash
npm install
```

### 3. Start MongoDB server
Ensure MongoDB is running locally at:
```
mongodb://127.0.0.1:27017/productDB
```

Example (Linux/macOS):
```bash
mongod
```

### 4. Run the server
```bash
node index.js
```

Or with nodemon (auto-restart):
```bash
npx nodemon index.js
```

### 5. Server will be available at
```
http://localhost:3000
```

---

## 📌 API Endpoints

### 1. ➕ Create Product
**POST** `/products`

**Body (JSON):**
```json
{
  "name": "Smartphone",
  "price": 699,
  "category": "Electronics"
}
```

**Response (201 Created):**
```json
{
  "_id": "64f9a1b2e3a4c5d6f7a8b901",
  "name": "Smartphone",
  "price": 699,
  "category": "Electronics",
  "__v": 0
}
```

---

### 2. 📖 Get All Products
**GET** `/products`

**Response (200 OK):**
```json
[
  {
    "_id": "64f9a1b2e3a4c5d6f7a8b901",
    "name": "Smartphone",
    "price": 699,
    "category": "Electronics"
  },
  {
    "_id": "64f9a1b2e3a4c5d6f7a8b902",
    "name": "Laptop",
    "price": 1200,
    "category": "Electronics"
  }
]
```

---

### 3. 🔍 Get Product by ID
**GET** `/products/:id`

**Response (200 OK):**
```json
{
  "_id": "64f9a1b2e3a4c5d6f7a8b901",
  "name": "Smartphone",
  "price": 699,
  "category": "Electronics"
}
```

---

### 4. ✏️ Update Product by ID
**PUT** `/products/:id`

**Body (JSON):**
```json
{
  "name": "Smartphone",
  "price": 649,
  "category": "Electronics"
}
```

**Response (200 OK):**
```json
{
  "_id": "64f9a1b2e3a4c5d6f7a8b901",
  "name": "Smartphone",
  "price": 649,
  "category": "Electronics"
}
```

---

### 5. 🗑️ Delete Product by ID
**DELETE** `/products/:id`

**Response (200 OK):**
```json
{
  "message": "Product deleted",
  "product": {
    "_id": "64f9a1b2e3a4c5d6f7a8b901",
    "name": "Smartphone",
    "price": 649,
    "category": "Electronics"
  }
}
```

---

## 🧪 Testing with Postman

1. Open **Postman** and set the base URL:  
   ```
   http://localhost:3000/products
   ```

2. Available requests:
   - `POST /products` → Create product  
   - `GET /products` → Get all products  
   - `GET /products/:id` → Get product by ID  
   - `PUT /products/:id` → Update product by ID  
   - `DELETE /products/:id` → Delete product by ID  

3. Set request **Body → raw → JSON** for POST/PUT requests.  
4. For GET/PUT/DELETE by ID, copy the `_id` value returned in POST response.  

---

## 🧰 Troubleshooting
- **MongoDB connection error** → ensure `mongod` service is running.  
- **CastError (ObjectId)** → check you passed a valid MongoDB `_id`.  
- **Validation error** → ensure `name`, `price`, and `category` are provided correctly.  

---

---

## 📷 Output Screenshots

![Screenshot](/OUTPUT/Screenshot%202025-10-05%20220044.png)
![Screenshot](/OUTPUT/Screenshot%202025-10-05%20220115.png)
![Screenshot](/OUTPUT/Screenshot%202025-10-05%20220225.png)
![Screenshot](/OUTPUT/Screenshot%202025-10-05%20220301.png)
![Screenshot](/OUTPUT/Screenshot%202025-10-05%20220345.png)

---


