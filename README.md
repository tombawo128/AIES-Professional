# AIES — Academic Internship Evaluation System

A web-based platform for managing and evaluating student internships. AIES connects students, workplace supervisors, and academic coordinators in one place, replacing paper-based evaluation forms with a simple digital workflow.

## Features

- **Supervisor evaluations** — supervisors submit structured performance reviews online
- **Coordinator dashboard** — track every student's internship status in one view
- **Student portal** — students can view their own progress and feedback
- **Standardized criteria** — consistent grading across professionalism, technical skill, and communication
- **Role-based access** — separate views/permissions for students, supervisors, and admins

## Tech Stack

- **Frontend:** Vite + React
- **Backend / Database:** Supabase

## Project Structure

```
AIES-professional/
├── frontend/aies-frontend/   # React app
└── backend/aies-backend/     # Backend / API
```

## Getting Started

1. Clone the repository
   ```
   git clone https://github.com/UpSkillHub/AIES-professional.git
   cd AIES-professional
   ```

2. Install dependencies (inside the frontend folder)
   ```
   cd frontend/aies-frontend
   npm install
   ```

3. Set up environment variables

   Create a `.env` file in `frontend/aies-frontend` with:
   ```
   VITE_SUPABASE_URL=your-supabase-project-url
   VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
   ```
   (Find these in your Supabase project under **Settings → API**.)

4. Run the app locally
   ```
   npm run dev
   ```

## Deployment

This project is deployed on [Vercel](https://vercel.com). When deploying, make sure to add the same environment variables (`VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY`) under your Vercel project's **Settings → Environment Variables**, then redeploy.

## License

This project is for academic/internship purposes.
