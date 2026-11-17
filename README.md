<div align="center">

# AIES — Academic Internship Evaluation System

**A digital internship evaluation workspace for students, workplace supervisors and university coordinators.**

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

[Live application](https://aies-professional.vercel.app/login) · [Repository issues](https://github.com/tombawo128/AIES-Professional/issues) · [Pull requests](https://github.com/tombawo128/AIES-Professional/pulls)

<img width="1919" alt="AIES dashboard" src="https://github.com/user-attachments/assets/d05a9a1a-a196-4911-b209-803c16fd4c87" />

</div>

---

## About

AIES replaces paper-based internship evaluation with a role-aware digital workflow. Students can follow their internship progress and feedback, workplace supervisors can submit evaluations, and university coordinators can monitor student placements and evaluation activity.

## Main capabilities

- **Student workspace:** view internship progress, reports and supervisor feedback.
- **Company workspace:** manage internship activity, interns and workplace evaluations.
- **University workspace:** manage students, departments, reports and academic evaluations.
- **Administrator workspace:** manage users, organisations, reports and system activity.
- **Authentication and access:** Supabase-backed sign-in and role-protected application areas.
- **Evaluation workflow:** structured evaluations using shared assessment criteria.

> Available features and permissions are enforced by the application and configured Supabase policies. Review the current implementation and database policies before using the system with real student records.

## Technology

| Area | Technology |
|---|---|
| Frontend | React 18, TypeScript, Vite |
| Routing | React Router |
| Backend and database | Supabase, PostgreSQL |
| Authentication | Supabase Auth |
| Hosting | Vercel |

## Repository structure

```text
AIES-Professional/
├── public/
│   ├── _redirects
│   └── favicon.svg
├── src/
│   ├── components/
│   ├── context/
│   ├── pages/
│   ├── App.tsx
│   ├── main.jsx
│   ├── styles.css
│   └── supabaseClient.ts
├── index.html
├── package.json
├── tsconfig.json
├── vite.config.js
└── vercel.json
```

## Local setup

### Requirements

- Node.js 20 or newer
- npm
- A Supabase project with the required application schema and access policies

### Install and run

Clone the repository and install dependencies:

```bash
git clone https://github.com/tombawo128/AIES-Professional.git
cd AIES-Professional
npm install
```

Create a `.env.local` file in the repository root:

```env
VITE_SUPABASE_URL=https://YOUR_PROJECT_REF.supabase.co
VITE_SUPABASE_ANON_KEY=YOUR_SUPABASE_PUBLISHABLE_OR_ANON_KEY
```

Use the publishable/anon key only. Never place a Supabase service-role or secret key in a `VITE_*` variable or browser code.

Start the development server:

```bash
npm run dev
```

Vite prints the local URL in the terminal, normally `http://localhost:5173`.

## Available scripts

| Command | Purpose |
|---|---|
| `npm run dev` | Start the local development server |
| `npm run build` | Run TypeScript checks and create the production build |
| `npm run preview` | Preview the production build locally |

Run the production build before deploying:

```bash
npm run build
```

## Supabase and security

The frontend connects to the Supabase project configured through the environment variables. Configure the required database schema, authentication settings and Row Level Security policies in that project.

- Keep service-role keys and other privileged secrets on trusted server-side infrastructure only.
- Enable and test RLS for every table exposed to the client.
- Verify that each role can access only its authorised records.
- Use test accounts for student, company, university and administrator workflows before production use.

This repository's frontend build does not verify the state of a connected Supabase project. Database policies, migrations, authentication redirects and production data access require separate verification.

## Deployment

The application is configured for Vercel.

1. Import `tombawo128/AIES-Professional` into Vercel.
2. Keep the repository root as the project Root Directory.
3. Add `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` to the required environments.
4. Confirm the Supabase authentication redirect URLs include the deployed application domain.
5. Deploy only after the production build and role-based access checks pass.

The repository includes `vercel.json` and `public/_redirects` for application routing. Verify direct navigation and refresh on protected routes after deployment.

## Screenshots

The dashboard screenshot above shows the application interface. Add current student, company, university and administrator screenshots here as those views are reviewed.

## Contributing

1. Create a feature branch from `master`.
2. Keep changes focused and include relevant tests or verification notes.
3. Run `npm run build`.
4. Open a pull request describing the change and any database or environment requirements.

## License

No explicit open-source license is currently declared. All rights remain with the repository owner unless a license is added.
