# DevPulse API

A RESTful backend API for an internal tech issue and feature tracker. Built for software teams to report bugs, suggest features, and coordinate resolutions.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Node.js (LTS) | Runtime environment |
| TypeScript (ESM) | Type-safe development |
| Express.js v5 | Web framework |
| PostgreSQL (NeonDB) | Relational database |
| Raw SQL (pg driver) | Database queries |
| bcrypt | Password hashing |
| jsonwebtoken | Authentication |
| http-status-codes | HTTP status references |

---

## 📁 Project Structure
src/
├── config/
│   └── db.ts              
├── middlewares/
│   └── auth.middleware.ts 
├── modules/
│   ├── auth/
│   │   ├── auth.controller.ts
│   │   └── auth.routes.ts
│   └── issues/
│       ├── issues.controller.ts
│       └── issues.routes.ts
├── utils/
│   ├── interfaces.ts      
│   ├── response.utils.ts  
│   └── db.utils.ts       
├── app.ts                
└── server.ts    

## 👥 User Roles & Permissions

| Role | Permissions |
|------|------------|
| contributor | Register, login, create issues, view issues, update own open issues |
| maintainer | All contributor permissions + update any issue, delete any issue |

---

## ⚙️ Local Setup

### 1. Clone the repository

```bash
git clone https://github.com/Fahim7600/devpulse-api.git
cd devpulse-api
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create `.env` file in root

```env
PORT=5000
DATABASE_URL=your_neondb_connection_string
JWT_SECRET=your_secret_key
```

### 4. Run database schema

Go to your NeonDB SQL Editor and run the contents of `schema.sql`

### 5. Start development server

```bash
npm run dev
```

Server runs at `http://localhost:5000`


## 🚀 Deployment

This API is deployed on **Render**.

Live URL: `https://devpulse-api.onrender.com`

