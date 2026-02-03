# 🏥 Hospital Management System

A full-stack hospital appointment management system that allows patients to book appointments and enables admins to review, approve, or reject them with built-in conflict prevention and dynamic availability handling.

This project is designed to simulate a **real-world healthcare workflow**, focusing on clean architecture, role-based access, and data integrity rather than just UI.

---

## ✨ Key Features

### 👤 Patient Side
- Book hospital appointments through a simple React interface
- Automatic validation for required fields
- Smart handling of unavailable dates with **next available date suggestions**
- Appointments are created in a **pending** state by default

### 🛠 Admin Side
- Secure admin login using **JWT authentication**
- View all appointments in a centralized dashboard
- Approve or reject appointments
- Prevents approving conflicting appointments for the same doctor and date
- Only **approved appointments block availability**

### 🧠 Smart Logic
- Dynamic availability (no hardcoded schedules)
- Date conflicts are calculated from existing **approved appointments**
- Rejected appointments do not block future bookings
- Clean separation between business logic and UI

---

## 🧱 Tech Stack

### Frontend
- React
- React Router
- Fetch API
- Modern component-based UI structure

### Backend
- Node.js
- Express.js
- MongoDB + Mongoose
- JWT Authentication
- RESTful API design

### Database
- MongoDB (Appointments, Doctors, Admin logic)

---

## 🏗 Project Architecture

This project is split into **three repositories** for clarity and scalability:

### 🔹 Main Repository (This Repo)
Acts as the **project overview and documentation hub**, linking the frontend and backend while explaining the system design.

### 🔹 Frontend Repository
📁 **hospital-react-client**  
Handles all UI logic, form validation, admin dashboard, and API interactions.

### 🔹 Backend Repository
📁 **hospital-server**  
Implements REST APIs, authentication, appointment logic, admin controls, and database operations.

---

## 🔐 Security & Access Control

- JWT-based authentication for admin routes
- Protected API endpoints using middleware
- Admin-only privileges enforced on the backend
- Frontend access alone cannot bypass backend authorization

---

## 📌 Appointment Flow (High Level)

1. Patient submits appointment request
2. Appointment is stored as **pending**
3. Admin reviews the request
4. Admin approves or rejects
5. Only **approved** appointments block a doctor’s date
6. Conflicting approvals are prevented automatically

---

## 🚀 Why This Project Matters

This project goes beyond CRUD:
- Demonstrates **real-world backend decision logic**
- Shows understanding of **auth, roles, and data consistency**
- Built with scalability and clarity in mind
- Structured like a production-ready system, not a demo app

---

## 📂 Repositories

- 🔗 Frontend: `hospital-react-client`(https://github.com/Ayanokojl/Hospital-react-client)
- 🔗 Backend: `hospital-server`(https://github.com/Ayanokojl/hospital-server)

---

## 🧑‍💻 Author

Built by **Abhay**  
Focused on clean architecture, backend logic, and real-world problem solving.
