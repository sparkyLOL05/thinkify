# Thinkify 🚀

[![Vercel Deployment](https://img.shields.io/badge/Deploy-Vercel-black?style=flat-square&logo=vercel)](https://thinkify.vercel.app)
[![Render Backend](https://img.shields.io/badge/Backend-Render-darkblue?style=flat-square&logo=render)](https://thinkify-backend-bnh6.onrender.com)
[![Postman API Docs](https://img.shields.io/badge/API_Docs-Postman-orange?style=flat-square&logo=postman)](https://documenter.getpostman.com/view/27027258/2sA3dxEXJh)

Thinkify is a robust, full-stack web hub engineered to foster vibrant, cross-disciplinary collaboration, idea validation, and structured productivity. Architected as a decoupled multi-directory monorepo, the platform uses fine-grained role permissions, backend data aggregation pipelines, and secure token isolation to deliver a modern community experience.

---

## 🔗 Live Links & Preview

* **Live Frontend Web Client:** [https://thinkify.vercel.app](https://thinkify.vercel.app)
* **Production API Target Service:** [https://thinkify-backend-bnh6.onrender.com/api](https://thinkify-backend-bnh6.onrender.com/api)
* **Interactive API Playground:** [Postman Workspace View](https://documenter.getpostman.com/view/27027258/2sA3dxEXJh)

---

## 🛠️ Architectural Breakdown & Stack

The system decouples the layout layer from the data management container. Client components communicate via an asynchronous API bridge utilizing structured cross-origin configurations.

| Layer Domain | Component Responsibility | Technical Implementation Stack |
| :--- | :--- | :--- |
| **Frontend UI** | Static Client Interface | React.js (Vite Bundle Compiler), Axios Client, Tailwind CSS |
| **Backend API** | REST API Business Logic | Node.js, Express.js Web Framework, Cookie-Parser Middleware |
| **Database** | Managed Persistence | MongoDB Cloud Atlas (Mongoose ODM Framework) |
| **Deployment** | Production Infrastructure | Vercel (Edge Client Engine), Render (Dynamic Cloud Instances) |

---

## 💡 System Design & Core Engineering

### 🔐 Token-Isolated Session Security
* **Cryptographic Salting:** Credentials undergo one-way transformation using **Bcrypt multi-round salt generation algorithms** prior to database persistence.
* **XSS Defended Tracking:** Upon verification, credentials generate signed **JSON Web Tokens (JWT)** issued straight into the client environment via **HttpOnly cookies**, creating a barrier against cross-site scripting script injection vulnerabilities.

### 🛡️ Admin Dashboard & Telemetry Aggregations
* **System Control Center:** Administrative portals access dynamic user privilege tables for community platform regulation.
* **Database Telemetry Pipelines:** Utilizes native MongoDB computational aggregation matrices to parse registration numbers over the last 30 days alongside user role tier weights.

### 🎓 Dynamic Member Profiles & Utilities
* **Content Inventory Operations:** Full CRUD integration allows members to submit rich-text posts, curate custom products, or purge old records instantly.
* **Task Matrix Workspace:** Native client-side schedule tracker configured directly within profile layers to maintain personal operational deadlines.
* **Security Control Systems:** Profile-level sub-routing modules empowering users to manage self-serve rotation of account passwords.

---

## ⚙️ Project Environment Matrix

To launch this system locally or configure hosting environment dashboards, establish individual target variables using the parameters below:

### 📱 Frontend Config Container (`/client/.env`)
```env
VITE_SERVER_ENDPOINT=[https://thinkify-backend-bnh6.onrender.com/api](https://thinkify-backend-bnh6.onrender.com/api)
VITE_TOKEN_KEY=thinkify
VITE_USER_ROLE=role
VITE_COOKIE_EXPIRES=1
