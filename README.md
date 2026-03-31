#  Spring Boot JWT Authentication API

A secure REST API built using Spring Boot that implements JWT (JSON Web Token) based authentication and authorization with MySQL database integration.

---

## Features

-  User Authentication using JWT
-  Secure API endpoints
-  MySQL database integration
-  Spring Boot REST API
-  Token-based authorization
-  Layered architecture (Controller, Service, Repository)

---

## 🛠️ Tech Stack

- Java
- Spring Boot
- Spring Security
- JWT (JSON Web Token)
- MySQL
- Maven

---

## 📂 Project Structure
src/
├── controller

├── service

├── repository

├── security

└── model
---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/sakshii-1707/springboot-jwt-authentication-api.git
```
2️⃣ Configure MySQL

Create a database:

CREATE DATABASE jwt_demo;

Update application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/jwt_demo
spring.datasource.username=your_username
spring.datasource.password=your_password
3️⃣ Run the application

Run as Spring Boot App or:

mvn spring-boot:run
# API Endpoints
1. Login
POST /api/login

Body (x-www-form-urlencoded):

username=sakshi
password=1234

<img width="1449" height="721" alt="image" src="https://github.com/user-attachments/assets/3e204607-7d6c-4ad8-a32a-aa081bacecba" />


Response:

JWT Token
# Protected Endpoint
GET /api/hello

Headers:

Authorization: Bearer <JWT_TOKEN>

Response:

Hello! JWT Authentication Successful

<img width="1440" height="623" alt="image" src="https://github.com/user-attachments/assets/95ea5082-0695-491b-89f4-1eb63eca8917" />

# How It Works
User sends login credentials
Server validates user from database
JWT token is generated
Client sends token in header
Server verifies token before granting access
# Important Notes
Ensure MySQL is running
Insert user manually in users table:
INSERT INTO users (username, password) VALUES ('sakshi', '1234');
- Future Improvements
- Password encryption using BCrypt
- User registration API
- Token refresh mechanism
- Role-based authorization
  
👩‍💻 Author

Sakshi Kumari
