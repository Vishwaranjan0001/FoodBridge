# FoodBridge — Smart Food Management

A group project connecting food donors and NGOs to coordinate surplus-food redistribution. The repository contains a **React frontend** and a **Node.js / Express / MongoDB backend**.

[Developer profile](https://github.com/Vishwaranjan0001) · [Portfolio](https://vishwaranjan0001.github.io/)

## Features and engineering

- Donor and NGO account workflows, password hashing, and JWT authentication.
- Donation listings, details, and NGO-facing coordination screens.
- Donation feedback, impact views, and wishlist interface.
- Multer-based file uploads and Nodemailer email integration.

## Stack

JavaScript · React 18 · Vite · React Router · Express 5 · MongoDB / Mongoose · JWT · bcryptjs · Multer · Nodemailer.

## Repository layout

```text
App/
  backend/
    src/config/        Database connection
    src/controllers/   User, NGO, donation and feedback handlers
    src/middlewares/   JWT authentication
    src/models/        MongoDB models
    src/routes/        REST API routes
    src/utils/         Email transport
  frontend/
    src/pages/         Donor and NGO screens
    src/utils/         Client-side authentication helpers
```

## Run locally

Use Node.js 22+ and a running MongoDB instance.

```bash
git clone https://github.com/Vishwaranjan0001/FoodBridge.git
cd FoodBridge/App/backend
npm install
```

Create `App/backend/.env` inside your checkout using the safe example in that folder. Set a private `JWT_SECRET`, a MongoDB connection string in `DB_ADD`, and SMTP credentials if testing email.

```bash
npm run dev
```

In a second terminal, from the repository root:

```bash
cd App/frontend
npm install
npm run dev
```

Open the Vite URL printed in the terminal. The frontend currently calls the API at **http://localhost:5000**. A backend health route is mounted at `/api/health`.

## Review the source

Start with [server entry point](App/backend/src/server.js), [authentication middleware](App/backend/src/middlewares/jwt_auth.js), and [frontend pages](App/frontend/src/pages).

## Project scope

This is a group-project implementation intended for local demonstration. Features described above are based on the committed source; no production usage or impact metrics are claimed. The backend test script is currently a placeholder.
