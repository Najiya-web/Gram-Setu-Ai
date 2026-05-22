# GramSetuAi

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 19.2.19.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Karma](https://karma-runner.github.io) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.

# 🌾 Gram Setu AI - Backend Engine

Gram Setu AI is a robust, full-stack MVC (Model-View-Controller) application designed to bridge communication gaps for rural citizens. This repository houses the core Node.js (Express) backend server, handling authentication, report management, and secure cloud interactions.

## 🔗 Project Links
* **Live Web App**: [Gram Setu AI Frontend](https://netlify.app)
* **API Server Base**: `https://onrender.com`

---

## 🚀 Key Architectural Engineering

* **Decoupled Architecture**: Frontend static assets are deployed autonomously on Netlify's CDN network, while dynamic operations execute on a private Render server instance.
* **Seamless SPA Routing**: Implemented strict edge rewrite policies (`_redirects`) to guarantee consistent SPA link persistence and browser state refreshes.
* **Global Access & CORS Management**: Secure multi-origin handling allowing both `localhost` debugging profiles and safe cross-origin resource access.

---

## 🛠️ Architecture & Tech Stack

* **Runtime Environment**: Node.js
* **Web Framework**: Express.js (MVC Pattern)
* **Database Engine**: MongoDB Atlas (Cloud Instance)
* **ODM Layer**: Mongoose
* **Asset Engine**: Cloudinary V2 (Secure image processing)
* **Security Layer**: Cross-Origin Resource Sharing (`cors`), Environment Isolation (`dotenv`)

---

## 📁 Repository Structure

```text
express/
├── controllers/      # Route request logic handlers
├── models/           # Mongoose schemas & data modeling
├── routes/           # Express router path controllers
└── server.js         # Core application bootstrapper & configuration
```

---

## 📡 Core API Endpoints Reference

### Authentication & Registration
* **`POST /api/userregister/register`** - Registers a new citizen profile.
  ```json
  {
    "fullName": "Amin Salim Shaikh",
    "mobile": 9765890174,
    "aadhar": "555555551234",
    "village": "Wagholi",
    "taluka": "Haveli",
    "pincode": 412207,
    "password": "securePassword123"
  }
  ```
* **`POST /api/auth/login`** - Validates user credentials.

### Reports & Feedback
* **`POST /api/reports`** - Submits a rural issue ticket (supports Cloudinary attachments).
* **`POST /api/feedback`** - Logs citizen evaluation metrics.

