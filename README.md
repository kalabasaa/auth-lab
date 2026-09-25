<div align="center">

# Laravel Authentication Lab

### A Laravel-based authentication system built for Web Systems and Technologies

A simple academic project focused on implementing **user registration, login, logout, authentication middleware, routing, and protected pages** using Laravel, Breeze, and Livewire.

<br>

![Laravel](https://img.shields.io/badge/Laravel-13-FF2D20?style=for-the-badge\&logo=laravel\&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-8.3-777BB4?style=for-the-badge\&logo=php\&logoColor=white)
![Livewire](https://img.shields.io/badge/Livewire-4-4E56A6?style=for-the-badge\&logo=livewire\&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=for-the-badge\&logo=sqlite\&logoColor=white)

</div>

---

## About

**Laravel Authentication Lab** is a simple authentication application created as part of **Web Systems and Technologies**.

The project demonstrates how authentication works in Laravel through user registration, login, logout, and middleware-protected routes.

The application uses **Laravel Breeze** with **Livewire** and **Livewire Blaze** to provide the authentication interface and functionality.

---

## Features

* User Registration
* User Login
* User Logout
* Authentication Middleware
* Protected Dashboard
* Form Validation
* Session-based Authentication
* Password Hashing

---

## Screenshots

### Registration

![Registration](screenshots/registration.png)

### Login

![Login](screenshots/login.png)

### Dashboard

![Dashboard](screenshots/dashboard.png)

### Middleware-Protected Route

![Protected Route](screenshots/middleware.png)

---

## Database Schema

### `users`

| Column              | Type      | Constraints       |
| ------------------- | --------- | ----------------- |
| `id`                | BIGINT    | Primary Key       |
| `name`              | VARCHAR   | Required          |
| `email`             | VARCHAR   | Required, Unique  |
| `email_verified_at` | TIMESTAMP | Nullable          |
| `password`          | VARCHAR   | Required          |
| `remember_token`    | VARCHAR   | Nullable          |
| `created_at`        | TIMESTAMP | Laravel Timestamp |
| `updated_at`        | TIMESTAMP | Laravel Timestamp |

---

## Routes

| Method | Route        | Purpose                         |
| ------ | ------------ | ------------------------------- |
| GET    | `/register`  | Display registration page       |
| POST   | `/register`  | Process user registration       |
| GET    | `/login`     | Display login page              |
| POST   | `/login`     | Process user login              |
| GET    | `/dashboard` | Display authenticated dashboard |
| POST   | `/logout`    | Log out the authenticated user  |

---

## Middleware

The dashboard is protected using Laravel's built-in **`auth` middleware**.

Unauthenticated users who attempt to access the dashboard are redirected to the login page.

```php
Route::get('/dashboard', function () {
    return view('dashboard');
})->middleware('auth');
```

---

## Project Structure

```text
auth-lab/
│
├── app/
│   ├── Livewire/
│   │
│   └── Models/
│       └── User.php
│
├── database/
│   ├── migrations/
│   │   ├── create_users_table.php
│   │   └── create_sessions_table.php
│   │
│   └── database.sqlite
│
├── resources/
│   └── views/
│       ├── components/
│       │
│       ├── layouts/
│       │
│       └── pages/
│
├── routes/
│   ├── web.php
│   └── auth.php
│
├── .env
├── composer.json
├── package.json
└── README.md
```

---

## Course Information

**Course:** Web Systems and Technologies
**Laboratory:** Midterm Laboratory 1
**Topic:** Login, Registration, and Middleware Authentication in Laravel
**Academic Year:** 2026–2027
**Semester:** First Semester

---

## Developer

**Jhon Renier Tambogon**

BSIT Student
University of Eastern Pangasinan

Built for **Systems Integration and Architecture 1**.
