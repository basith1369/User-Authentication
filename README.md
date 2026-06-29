# ApexPlanet-Task1-User-Authentication

A PHP & MySQL web application implementing user registration, login, and session management — built as part of the **ApexPlanet Software Pvt. Ltd. 30-Day Web Development Internship (Task 1)**.

---


## 🛠 Tech Stack

- PHP (MySQLi)
- MySQL
- HTML5 / CSS3
- XAMPP / WAMP

---

## 📁 Project Structure

```
task1/
├── db.php           # MySQL database connection
├── setup.sql        # SQL script to create database & table
├── register.php     # User registration page
├── login.php        # User login page
├── dashboard.php    # Protected dashboard (session required)
├── logout.php       # Destroys session and redirects
└── README.md        # Project documentation
```

---

## ⚙️ Setup Instructions

### 1. Install XAMPP / WAMP
Download and install [XAMPP](https://www.apachefriends.org/) or [WAMP](https://www.wampserver.com/) and start **Apache** and **MySQL** services.

### 2. Clone / Copy Project
Place the project folder inside your server root:
- **XAMPP:** `C:/xampp/htdocs/task1/`
- **WAMP:** `C:/wamp64/www/task1/`

### 3. Create the Database
1. Open your browser and go to `http://localhost/phpmyadmin`
2. Click **SQL** in the top menu
3. Paste the contents of `setup.sql` and click **Go**

This will create:
- Database: `apex_intern`
- Table: `users` with columns → `id`, `name`, `email`, `password`, `created_at`

### 4. Configure Database Credentials
Open `db.php` and update if needed:
```php
define('DB_USER', 'root');   // your MySQL username
define('DB_PASS', '');       // your MySQL password (blank by default in XAMPP)
```

### 5. Run the Application
Open your browser and visit:
```
http://localhost/task1/register.php
```

---

## 🚀 Features

| Feature | Details |
|---|---|
| User Registration | Captures name, email, password |
| Password Hashing | Uses PHP `password_hash()` with BCRYPT |
| Email Uniqueness | Prevents duplicate registrations |
| User Login | Authenticates via `password_verify()` |
| Session Management | Stores user info in `$_SESSION` |
| Protected Routes | Dashboard redirects to login if not authenticated |
| Logout | Destroys session cleanly |
| Input Validation | Client-side (`required`, `minlength`) + Server-side (PHP) |
| Success/Error Messages | Shown after each action |

---

## 📸 Screenshots

> *(Add your screenshots here after running the project)*

- `db-table.png` — phpMyAdmin users table
- `register.png` — Registration page
- `register-success.png` — After successful registration
- `login.png` — Login page
- `dashboard.png` — Dashboard after login

---

## 🔐 Security Highlights

- Passwords are **never stored in plain text** — hashed using `password_hash(PASSWORD_BCRYPT)`
- All user inputs are **sanitized** with `htmlspecialchars()` before display
- **Prepared statements** used for all database queries (prevents SQL injection)
- Session is properly **destroyed on logout**

---

## 👨‍💻 Author

**Name:** Abdul Basith  
**Internship at:** ApexPlanet Software Pvt. Ltd.  
**Program:** Web Development — PHP & MySQL (30 Days)  
**Task:** Task 1 — Setup and Basic User Authentication




