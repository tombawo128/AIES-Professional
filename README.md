<div align="center">

# 🎓 AIES: Academic Internship Evaluation System

**Replacing paper evaluation forms with a simple, transparent digital workflow for students, supervisors, and academic coordinators.**

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

[Live Demo](https://aies-professional.vercel.app/login) · [Report a Bug](https://github.com/UpSkillHub/AIES-professional/issues) · [Request a Feature](https://github.com/UpSkillHub/AIES-professional/issues)

<!-- Add a screenshot or GIF of the dashboard here -->
<img width="1919" height="1079" alt="Screenshot 2026-11-08 131429" src="https://github.com/user-attachments/assets/d05a9a1a-a196-4911-b209-803c16fd4c87" />

</div>

---

## 📑 Table of Contents

- [About](#-about)
- [Features](#-features)
- [User Roles](#-user-roles)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📖 About

Managing internships on paper is slow, inconsistent, and hard to track. **AIES** brings students, workplace supervisors, and academic coordinators together in one web platform so that evaluations are submitted online, graded against the same criteria, and visible to the right people at the right time.

---

## ✨ Features

- 📝 **Supervisor Evaluations**: submit structured performance reviews online
- 📊 **Coordinator Dashboard**: track every student's internship status in a single view
- 🎒 **Student Portal**: students view their own progress and supervisor feedback
- ⚖️ **Standardized Criteria**: consistent grading across professionalism, technical skill, and communication
- 🔐 **Role-Based Access**: separate views and permissions for students, supervisors, and admins

---

## 👥 User Roles

| Role | What they can do |
|------|------------------|
| **Student** | View personal internship progress and feedback |
| **Supervisor** | Submit and manage evaluations for their interns |
| **Coordinator / Admin** | Monitor all students, track statuses, and oversee evaluations |

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React, Vite |
| **Backend / Database** | Supabase (PostgreSQL, Auth, API) |
| **Hosting** | Vercel |

---

## 📂 Project Structure

```
AIES-professional/
├── frontend/
│   └── aies-frontend/    # React + Vite application
└── backend/
    └── aies-backend/     # Backend / API
```

---

## 🚦 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- npm (bundled with Node.js)
- A free [Supabase](https://supabase.com/) project

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/UpSkillHub/AIES-professional.git
cd AIES-professional
```

**2. Install frontend dependencies**

```bash
cd frontend/aies-frontend
npm install
```

**3. Configure environment variables**

Create a `.env` file in `frontend/aies-frontend` (see [Environment Variables](#-environment-variables)).

**4. Start the development server**

```bash
npm run dev
```

Open the local URL printed in your terminal (usually `http://localhost:5173`).

### Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the development server |
| `npm run build` | Create a production build |
| `npm run preview` | Preview the production build locally |

---

## 🔑 Environment Variables

Create `frontend/aies-frontend/.env`:

```env
VITE_SUPABASE_URL=your-supabase-project-url
VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
```

Find both values in your Supabase project under **Settings → API**.

> ⚠️ **Security note:** Never commit your `.env` file, and never expose the Supabase `service_role` key in frontend code. Protect your data with Supabase **Row Level Security (RLS)** policies so each role only sees what it should.

---

## ☁️ Deployment

AIES is deployed on [Vercel](https://vercel.com).

1. Import the repository into Vercel and set the **Root Directory** to `frontend/aies-frontend`.
2. Add these under **Settings → Environment Variables**:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
3. Redeploy so the variables take effect.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📜 License

This project is for academic and internship purposes.

---

<div align="center">

Built by [UpSkillHub](https://github.com/UpSkillHub) · ⭐ Star this repo if you find it useful!

</div>
