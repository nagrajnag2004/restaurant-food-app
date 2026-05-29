# 🍔 Restaurant Food Delivery Backend API

A production-ready RESTful Backend API for a Multi-Vendor Food Delivery Platform built using Node.js, Express.js, MongoDB, and JWT Authentication. The application enables users to register, authenticate, browse restaurants, manage food items and categories, place orders, and track order status through a secure and scalable backend architecture.

---

## 📌 Overview

This project demonstrates backend development concepts including:

* RESTful API Design
* Authentication & Authorization
* Role-Based Access Control (RBAC)
* MongoDB Database Modeling
* Middleware Implementation
* Order Management System
* MVC Architecture
* Secure Password Hashing
* API Testing & Validation

The system supports multiple entities such as Users, Restaurants, Categories, Food Items, and Orders while maintaining a clean and scalable code structure.

---

## 🚀 Key Features

### 🔐 Authentication & Security

* User Registration
* User Login
* JWT-Based Authentication
* Password Encryption using Bcrypt.js
* Protected Routes
* Role-Based Authorization (Admin & Customer)

### 👤 User Management

* Get User Profile
* Update User Information
* Update Password
* Reset Password
* Delete Account

### 🏪 Restaurant Management

* Create Restaurant
* Get All Restaurants
* Get Restaurant Details
* Delete Restaurant

### 🍕 Food Management

* Create Food Item
* Get All Foods
* Get Single Food Details
* Get Foods by Restaurant
* Update Food Information
* Delete Food Item

### 📂 Category Management

* Create Category
* Get All Categories
* Update Category
* Delete Category

### 📦 Order Management

* Place Food Orders
* Order Tracking
* Update Order Status
* Admin Order Control

---

## 🛠️ Tech Stack

### Backend Technologies

* Node.js
* Express.js

### Database

* MongoDB
* Mongoose ODM

### Authentication & Security

* JSON Web Token (JWT)
* Bcrypt.js

### API Testing

* Postman

### Development Tools

* Nodemon
* Git
* GitHub

---

## 📁 Project Structure

```bash
restaurant-food-app/
│
├── config/
│   └── db.js
│
├── controllers/
│   ├── authControllers.js
│   ├── userController.js
│   ├── foodController.js
│   ├── categoryController.js
│   └── restaurantController.js
│
├── middlewares/
│   ├── authMiddleware.js
│   └── adminMiddleware.js
│
├── models/
│   ├── userModel.js
│   ├── foodModel.js
│   ├── categoryModel.js
│   ├── restaurantModel.js
│   └── orderModel.js
│
├── routes/
│   ├── authRoutes.js
│   ├── userRoutes.js
│   ├── foodRoutes.js
│   ├── categoryRoutes.js
│   └── restaurantRoutes.js
│
├── .env
├── package.json
├── server.js
│
└── README.md
```

---

## 🗄️ Database Models

### User

```javascript
{
  userName,
  email,
  password,
  phone,
  address,
  userType
}
```

### Restaurant

```javascript
{
  title,
  imageUrl,
  rating,
  delivery,
  pickup,
  location
}
```

### Category

```javascript
{
  title,
  imageUrl
}
```

### Food

```javascript
{
  title,
  description,
  price,
  category,
  restaurant,
  imageUrl
}
```

### Order

```javascript
{
  foods,
  buyer,
  payment,
  status
}
```

---

## 🔑 Authentication Flow

1. User registers an account.
2. Password is securely hashed using Bcrypt.js.
3. User logs in with valid credentials.
4. JWT token is generated and returned.
5. Protected routes verify JWT tokens.
6. Role-based middleware restricts admin-only operations.

---

## 📡 API Endpoints

### Authentication

```http
POST /api/v1/auth/register
POST /api/v1/auth/login
```

### User APIs

```http
GET    /api/v1/user/getUser
PUT    /api/v1/user/updateUser
POST   /api/v1/user/updatePassword
POST   /api/v1/user/resetPassword
DELETE /api/v1/user/deleteUser/:id
```

### Restaurant APIs

```http
POST   /api/v1/resturant/create
GET    /api/v1/resturant/getAll
GET    /api/v1/resturant/get/:id
DELETE /api/v1/resturant/delete/:id
```

### Category APIs

```http
POST   /api/v1/category/create
GET    /api/v1/category/getAll
PUT    /api/v1/category/update/:id
DELETE /api/v1/category/delete/:id
```

### Food APIs

```http
POST   /api/v1/food/create
GET    /api/v1/food/getAll
GET    /api/v1/food/get/:id
GET    /api/v1/food/getByResturant/:id
PUT    /api/v1/food/update/:id
DELETE /api/v1/food/delete/:id
```

### Order APIs

```http
POST /api/v1/food/placeorder
POST /api/v1/food/orderStatus/:id
```

---

## ⚙️ Installation & Setup

### Clone Repository

```bash
git clone https://github.com/nagrajnag2004/restaurant-food-app.git
```

### Navigate to Project Directory

```bash
cd your-repo-name
```

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a `.env` file in the root directory.

```env
PORT=5000
MONGO_URI=YOUR_MONGODB_URI
JWT_SECRET=YOUR_SECRET_KEY
```

### Start Development Server

```bash
npm run dev
```

### Start Production Server

```bash
npm start
```

---

## 🧪 Testing

All APIs were tested using Postman.

Testing includes:

* Authentication Validation
* Protected Route Verification
* CRUD Operations
* Database Integration
* Order Workflow Testing
* Error Handling

---

## 📈 Future Improvements

* Online Payment Gateway Integration
* Restaurant Dashboard
* Food Reviews & Ratings
* Image Upload using Cloudinary
* Real-Time Order Tracking
* Delivery Partner Module
* Email Notifications
* Swagger API Documentation

---

## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

* Backend Development with Node.js & Express.js
* RESTful API Design
* MongoDB Database Modeling
* JWT Authentication
* Middleware Architecture
* Secure Password Management
* MVC Project Structure
* API Testing using Postman
* Git & GitHub Version Control

---

## 👨‍💻 Author

### Nagraj Nag

B.Tech Computer Science & Engineering

📧 Open to Software Development, Backend Development, and Full-Stack Opportunities.

### Connect With Me

GitHub:
https://github.com/nagrajnag2004

LinkedIn:
https://www.linkedin.com/in/nagraj-nag-b66459272

---

⭐ If you found this project helpful, consider giving it a star on GitHub.
