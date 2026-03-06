# 🏥 Schedula Backend - Task 4

Backend authentication and user onboarding system built using **NestJS, Prisma, and PostgreSQL**.  
This project implements secure user authentication with **JWT**, password hashing, and role-based onboarding for **Doctors and Patients**.

---

## 🚀 Tech Stack

- **Node.js**
- **NestJS**
- **Prisma ORM**
- **PostgreSQL**
- **JWT Authentication**
- **bcrypt for password hashing**
- **Thunder Client / Postman for API testing**

---

## 📂 Project Structure


src
├── auth
│ ├── auth.controller.ts
│ ├── auth.service.ts
│ ├── auth.module.ts
│ ├── jwt.strategy.ts
│
├── prisma
│ ├── prisma.module.ts
│ ├── prisma.service.ts
│
├── app.controller.ts
├── app.module.ts
├── main.ts

prisma
├── schema.prisma


---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository


git clone https://github.com/KumarManglam-123/schedula-backend-task4

cd schedula-backend-task4


---

### 2️⃣ Install dependencies


npm install


---

### 3️⃣ Configure Environment Variables

Create `.env` file:


DATABASE_URL="postgresql://postgres:password@localhost:5432/schedula"
JWT_SECRET="secret123"


---

### 4️⃣ Run Prisma Migration / Sync


npx prisma db push


---

### 5️⃣ Start the backend server


npm run start:dev


Server will run on:


http://localhost:3000


---

### 6️⃣ Open Prisma Studio (Database UI)


npx prisma studio


Open:


http://localhost:5555


---

## 🔐 Authentication APIs

### Signup User


POST /auth/signup


Example Request Body:


{
"email": "doctor@gmail.com
",
"password": "doctor123",
"role": "DOCTOR"
}


Or


{
"email": "patient@gmail.com
",
"password": "patient123",
"role": "PATIENT"
}


---

### Signin User


POST /auth/signin


Example Request Body:


{
"email": "doctor@gmail.com
",
"password": "doctor123"
}


Response:


{
"access_token": "JWT_TOKEN"
}


---

## 👨‍⚕️ User Roles

The system supports two roles:

- **DOCTOR**
- **PATIENT**

These roles allow onboarding of different user types in the scheduling system.

---

## 🔒 Security Features

- Passwords hashed using **bcrypt**
- **JWT Authentication**
- Environment variables for secrets
- Role-based user structure

---

## 🧪 Testing

APIs were tested using:

- **Thunder Client (VS Code)**
- **Prisma Studio**

---

## 📌 Features Implemented

✔ User Signup  
✔ User Signin  
✔ JWT Authentication  
✔ Password Hashing (bcrypt)  
✔ Prisma ORM Integration  
✔ PostgreSQL Database  
✔ Doctor and Patient onboarding

---

## 📧 Author

**Kumar Manglam**

Backend Developer | Node.js | NestJS | Prisma

GitHub:  
https://github.com/KumarManglam-123