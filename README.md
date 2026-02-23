# 🛒 E-Commerce Backend API

A scalable and production-ready backend system for managing an e-commerce product catalog.

Built with:

* Django
* PostgreSQL (production-ready)
* JSON Web Token (JWT)
* Swagger for API docs

---

## 🚀 Features

### ✅ Authentication

* User Registration
* JWT Login
* Token Refresh
* Secure protected endpoints

### ✅ Product Management

* Create, Read, Update, Delete (CRUD)
* Categories management
* Admin-controlled write access

### ✅ Advanced API Features

* Filtering by category
* Sorting by price
* Search by product name
* Pagination (10 items per page)

### ✅ Performance Optimized

* Indexed fields
* Optimized queries with `select_related`
* PostgreSQL ready

---

## 📁 Project Structure

```
ecommerce_backend/
│
├── config/          # Project configuration
├── users/           # Authentication logic
├── products/        # Product & category management
├── manage.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone <your-repository-url>
cd ecommerce_backend
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Configure Environment Variables

Create a `.env` file:

```
SECRET_KEY=your-secret-key
DB_NAME=ecommerce_db
DB_USER=postgres
DB_PASSWORD=yourpassword
DB_HOST=localhost
DB_PORT=5432
```

### 5️⃣ Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6️⃣ Create Superuser

```bash
python manage.py createsuperuser
```

### 7️⃣ Run Server

```bash
python manage.py runserver
```

---

## 📘 API Documentation

Swagger UI available at:

```
http://127.0.0.1:8000/swagger/
```

ReDoc:

```
http://127.0.0.1:8000/redoc/
```

---

## 🔐 Authentication Endpoints

| Method | Endpoint               | Description   |
| ------ | ---------------------- | ------------- |
| POST   | `/api/users/register/` | Register user |
| POST   | `/api/token/`          | Obtain JWT    |
| POST   | `/api/token/refresh/`  | Refresh JWT   |

Use the returned `access` token in headers:

```
Authorization: Bearer <your-token>
```

---

## 🛍 Product Endpoints

| Method | Endpoint              |
| ------ | --------------------- |
| GET    | `/api/products/`      |
| POST   | `/api/products/`      |
| GET    | `/api/products/{id}/` |
| PUT    | `/api/products/{id}/` |
| DELETE | `/api/products/{id}/` |

---

## 🔎 Filtering & Sorting Examples

Filter by category:

```
/api/products/?category=1
```

Sort by price:

```
/api/products/?ordering=price
/api/products/?ordering=-price
```

Search:

```
/api/products/?search=laptop
```

Pagination:

```
/api/products/?page=2
```

---

## 🧪 Running Tests

```bash
python manage.py test
```

---

## 🚀 Deployment

For production:

* Set `DEBUG = False`
* Use PostgreSQL
* Configure `ALLOWED_HOSTS`
* Store secrets in environment variables

Recommended platforms:

* Render
* Railway
* DigitalOcean

---

## 📌 Evaluation Criteria Covered

✔ CRUD APIs
✔ JWT Authentication
✔ Filtering, Sorting, Pagination
✔ Database Optimization
✔ Clean Architecture
✔ Swagger Documentation
✔ Version Control Ready

---

## 👨‍💻 Author

Ermias Dagnew
Backend Developer | Django | REST APIs

