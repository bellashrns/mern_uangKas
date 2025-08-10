# Uang Kas Management (MERN)

This repository contains the **backend** of a MERN (MongoDB, Express, React, Node) application for managing monthly cash contributions ("Uang Kas") within an organisation.  
The API provides authentication and role‑based access, user management, file uploads for proof of payment, and endpoints to create, read, update and delete cash records.

## Features

### Authentication and Session Management
- User registration and login with encrypted passwords (bcrypt).
- JWT‑based authentication with access token verification middleware.
- Role‑based authorisation (e.g., admin, member).

### Cash Contribution Management
- Create new cash records with amount, date, and notes.
- Upload proof of payment images.
- Update payment status (e.g., pending, approved, rejected).
- Retrieve transaction history by user or all records (admin).

### User Management
- Admin can view, update, and delete user accounts.
- Retrieve all registered users.
- Change user roles.

## Tech Stack
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ODM)
- **Authentication**: JWT, bcrypt
- **File Uploads**: Multer
- **Other**: dotenv for environment variables

## API Structure
```
controllers/       # Business logic for authentication, users, and cash records
middleware/        # JWT verification and role checking
models/            # Mongoose models (User, UangKas)
routes/            # Express route definitions
uploads/           # Stored proof-of-payment images
index.js           # Main Express app entry point
```

## Getting Started

### Prerequisites
- Node.js >= 18.x
- MongoDB database (local or cloud via MongoDB Atlas)
- npm or yarn package manager

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mern_uangKas.git
   ```
2. Navigate to the project folder:
   ```bash
   cd mern_uangKas
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Configure environment variables in `.env`:
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/uangkasdb
   JWT_SECRET=your_jwt_secret
   ```
5. Start the server:
   ```bash
   npm start
   ```
