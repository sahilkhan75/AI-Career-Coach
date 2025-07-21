# 🤖 AI Career Coach

AI Career Coach is a web-based, AI‑powered career guidance platform built with **Next.js 15**, **Tailwind CSS**, and a modern Node/Prisma backend. It helps users with **career advice, interview preparation, resume & cover‑letter generation, skill tracking, and personalized learning roadmaps** through an interactive AI experience.

---

## 🚀 Features

* AI‑assisted **Resume Builder** (ATS‑friendly output).
* AI **Cover Letter Generator**.
* **Mock Interview** module with question banks & performance tracking.
* **Dashboard** for skills, quizzes, stats, and user onboarding progress.
* Secure **auth flows** (sign‑in / sign‑up) with session handling.
* Responsive, accessible UI built with Tailwind + ShadCN components.
* Prisma ORM models for user, resume data, interviews, and more.

---

## 🛠 Tech Stack

**Frontend**: Next.js 15, React, Tailwind CSS, ShadCN UI, Recharts.

**Backend**: Node.js (API routes / server actions), Prisma ORM.

**Database**: PostgreSQL (update if you’re using another DB).

**Auth**: NextAuth.js (or your custom auth strategy—update as needed).

**AI Integration**: OpenAI API (swap/extend for other LLM providers).

**Deployment**: Vercel (recommended) or custom Node hosting.

---

## 📁 Project Structure (high level)

```
ai-career-coach/
├─ app/
│  ├─ (auth)/            # Sign-in / sign-up layouts & pages
│  ├─ (main)/            # Authenticated app areas: dashboard, resume, etc.
│  ├─ api/               # Route handlers (e.g., inngest)
│  ├─ globals.css        # Global styles
│  ├─ layout.js          # Root layout
│  └─ page.js            # Landing page
├─ actions/              # Server actions (cover letter, resume, interview, user)
├─ components/           # Reusable UI + layout components
├─ data/                 # Static data (FAQs, features, etc.)
├─ lib/                  # Helpers, prisma client, inngest client/functions
├─ prisma/               # Schema + migrations
├─ public/               # Static assets (images, icons)
├─ tailwind.config.mjs   # Tailwind config
├─ next.config.mjs       # Next.js config
└─ ...
```

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/sahilkhan75/AI-Career-Coach.git
cd AI-Career-Coach
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Variables

Create a `.env` file in the project root. Include (edit to match your setup):

```
# App
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your_nextauth_secret

# OpenAI / AI Provider
OPENAI_API_KEY=your_openai_key

# Database
DATABASE_URL=postgresql://user:password@host:5432/dbname

# (Optional) Inngest / other integrations
INNGEST_SIGNING_KEY=your_key_here
```

> Never commit real secrets. Your `.gitignore` should already exclude `.env`.

---

### 4. Database Setup (Prisma)

Run Prisma migrations to create your schema:

```bash
npx prisma migrate dev
# or, if db is already provisioned:
npx prisma db push
```

Generate Prisma Client:

```bash
npx prisma generate
```

---

### 5. Development Server

```bash
npm run dev
```

Visit: [http://localhost:3000](http://localhost:3000)

---

### 6. Production Build & Start

```bash
npm run build
npm start
```

This creates the `.next` production build (not committed to Git).

---

## 🔐 Authentication Notes

The project includes an `(auth)` route group for sign‑in/sign‑up flows. Update providers in your auth config (e.g., Email, Credentials, Google, GitHub) as required.

---

## 🤖 AI Modules

| Module         | Description                                  | Related Dir                                              |
| -------------- | -------------------------------------------- | -------------------------------------------------------- |
| Resume Builder | Collects user data & generates resume output | `app/(main)/resume` + `actions/resume.js`                |
| Cover Letter   | Generates tailored cover letters for roles   | `app/(main)/ai-cover-letter` + `actions/cover-letter.js` |
| Mock Interview | Quiz / Q\&A / scoring flows                  | `app/(main)/interview` + `actions/interview.js`          |
| Dashboard      | Aggregated stats & onboarding                | `app/(main)/dashboard` + `actions/dashboard.js`          |

---

## 🧪 Scripts (package.json)

Make sure your `package.json` has these (adjust if different):

```json
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  }
}
```

---

## 🚀 Deploying to Vercel

1. Push your repo to GitHub.
2. Import into Vercel.
3. Add environment variables in Vercel dashboard.
4. Deploy.

> Do **not** upload `.next` or `node_modules` to Git—they are built during deployment.


---

## 🌐 Live Demo

<!-- Update this URL if different -->

[AI Career Coach – Live](https://ai-career-coach-nu-ten.vercel.app/)

---

## 🧑‍💻 Author

**Sahil Khan**
Full Stack Web Developer (MERN / Next.js)

* GitHub: [sahilkhan75](https://github.com/sahilkhan75)
* LinkedIn: [sahilkhan75](https://www.linkedin.com/in/sahil-khan-74a08635b/)
* Email: [sahilkhan75](sahilkhangoryan@gmail.com)


