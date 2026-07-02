# 📅 Calendar Booking

![CI](https://img.shields.io/github/actions/workflow/status/NikitaSukharev/python-project-386/ci.yml?branch=main)
![Go](https://img.shields.io/badge/Go-1.24-00ADD8?logo=go&logoColor=white)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)
![OpenAPI](https://img.shields.io/badge/OpenAPI-3.0-6BA539)
![License](https://img.shields.io/badge/License-MIT-green)

A modern appointment booking application inspired by **Cal.com**.

The project follows the **Design First** approach: the API contract is defined first using **TypeSpec/OpenAPI**, followed by the implementation of the backend, frontend, automated testing, Docker support, and CI.

---

# ✨ Features

- 📅 Create meeting types
- ⏰ Book available time slots
- 🚫 Prevent double booking
- 👤 Admin dashboard
- 📖 OpenAPI & TypeSpec contract
- ⚡ Fast Go backend
- ⚛️ React + TypeScript frontend
- 🧪 End-to-End tests with Playwright
- 🐳 Docker support
- 🚀 GitHub Actions CI

---

# 🏗 Architecture

```
                +------------------+
                | React Frontend   |
                +------------------+
                         │
                    REST API
                         │
                +------------------+
                |    Go Backend    |
                +------------------+
                         │
                 In-Memory Storage
```

---

# 🚀 Live Demo

Application

https://xhrobj-ai-cal-386.onrender.com

Health Check

https://xhrobj-ai-cal-386.onrender.com/health

---

# 📖 User Flow

1. Open the **Admin Dashboard**.
2. Create a new meeting type.
3. Open the public booking page.
4. Select a meeting type.
5. Choose an available time slot.
6. Confirm the booking.
7. View the booking in the admin dashboard.

---

# 🛠 Tech Stack

| Layer | Technology |
|--------|------------|
| Backend | Go |
| Frontend | React 19 + TypeScript + Vite |
| API Contract | TypeSpec + OpenAPI |
| Testing | Go Tests + Playwright |
| CI/CD | GitHub Actions |
| Deployment | Docker + Render |

---

# 📂 Project Structure

```
backend/
    cmd/
    internal/

frontend/
    src/

contracts/
    openapi/
    typespec/

docs/

.github/
```

---

# ⚙️ Local Development

## Requirements

- Go 1.24+
- Node.js
- npm

Install dependencies

```bash
npm install
npm --prefix frontend install
```

Run backend

```bash
cd backend
go run ./cmd/api
```

Run frontend

```bash
cd frontend
npm run dev
```

The application will be available at

Frontend

```
http://127.0.0.1:5173
```

Admin

```
http://127.0.0.1:5173/admin
```

Backend

```
http://localhost:8080
```

Health Check

```
http://localhost:8080/health
```

---

# 🐳 Docker

Build

```bash
docker build -t calendar-booking .
```

Run

```bash
docker run --rm -e PORT=8080 -p 8080:8080 calendar-booking
```

---

# ✅ Available Checks

```bash
npm run check:contracts
npm run check:backend
npm run check:frontend
npm run test:e2e
```

Install Playwright browser (first run only)

```bash
npm run test:e2e:setup
```

---

# 🚧 Current Limitations

- No authentication
- Single calendar owner
- No external calendar integrations
- In-memory storage
- No edit/delete for meeting types
- Booking window limited to 14 days
- UTC-only time calculations

---

# 📄 API Contract

The API is designed using a **Design First** workflow.

```
TypeSpec
      │
      ▼
OpenAPI
      │
      ▼
Backend
      │
      ▼
Frontend
```

---

# 🔄 CI Pipeline

Every push automatically runs:

- Backend tests
- Frontend build
- API contract validation
- End-to-End tests

---

# 👨‍💻 Author

**Nikita Sukharev**

GitHub: https://github.com/NikitaSukharev

---

## Hexlet

This project was developed as part of the **AI for Developers** course by Hexlet.