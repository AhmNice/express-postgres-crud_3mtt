Here's a complete `README.md` file for your Express + PostgreSQL CRUD API project:

---

```markdown
# User Management API with Express and PostgreSQL (3MTT ASSIGNMENT)

This is a simple RESTful API built with **Express.js** and **PostgreSQL** that allows you to manage users. It supports full CRUD operations: Create, Read, Update, and Delete users.

## 📦 Features

- Get all users
- Get a user by ID
- Create a new user
- Update a user by ID
- Delete a user

## 🛠 Tech Stack

- Node.js
- Express.js
- PostgreSQL
- body-parser

## 📁 Project Structure

```

project/
│
├── db.js            # PostgreSQL pool connection
├── index.js         # Main server file (this code)
├── package.json
└── README.md

````

## 📄 API Endpoints

### GET `/users`

Fetch all users.

**Response:**
```json
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "age": 30
  }
]
````

---

### GET `/users/:id`

Fetch a single user by ID.

---

### POST `/users`

Create a new user.

**Request Body:**

```json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "age": 25
}
```

---

### PUT `/users/:id`

Update a user by ID.

**Request Body:**

```json
{
  "name": "Jane Doe Updated",
  "email": "jane@newmail.com",
  "age": 26
}
```

---

### DELETE `/users/:id`

Delete a user by ID.

---

## ⚙️ Setup Instructions

1. **Clone the repo**

   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Create PostgreSQL Database and Table**

   ```sql
   CREATE TABLE users (
     id SERIAL PRIMARY KEY,
     name VARCHAR(100),
     email VARCHAR(100) UNIQUE,
     age INT
   );
   ```

4. **Set up `db.js` connection**
   Create a `db.js` file with your PostgreSQL config:

   ```js
   import pkg from 'pg';
   const { Pool } = pkg;

   const pool = new Pool({
     user: 'your_user',
     host: 'localhost',
     database: 'your_db',
     password: 'your_password',
     port: 5432,
   });

   export default pool;
   ```

5. **Run the app**

   ```bash
   node index.js
   ```

   The server runs on `http://localhost:3000`

---



---

> Made with ❤️ using Express and PostgreSQL

```

---
