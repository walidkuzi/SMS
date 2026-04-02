# 🏫 School Management System

A role-based school administration dashboard built with **Next.js 14**, **TypeScript**, and **Tailwind CSS**.

---

## ✨ Features

- **Role-based navigation** — four roles: `admin`, `teacher`, `student`, `parent`, each with their own menu visibility
- **Entity management** — Teachers, Students, Parents, Subjects, Classes, Lessons
- **Academic tracking** — Exams, Assignments, Results
- **Attendance** tracking per student and class
- **Timetable / Calendar** with weekly lesson events
- **Communication** — Messages and Announcements
- **School Events** with class assignment and time slots
- **Strict TypeScript** throughout, Tailwind CSS utility-first UI

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Framework | [Next.js 14](https://nextjs.org/) (App Router) |
| Language | [TypeScript 5](https://www.typescriptlang.org/) |
| Styling | [Tailwind CSS 3](https://tailwindcss.com/) |
| UI Library | [React 18](https://react.dev/) |
| Font | Inter via `next/font/google` |
| Linting | ESLint + `eslint-config-next` (core-web-vitals) |

---

## 📁 Project Structure

```
SMS/
├── public/              # Static PNG icons and images
├── src/
│   ├── app/
│   │   ├── layout.tsx   # Root layout — metadata, font, <html>
│   │   ├── page.tsx     # Homepage (/ route)
│   │   └── globals.css  # Tailwind base/component/utility layers
│   ├── components/
│   │   └── Menu.tsx     # Sidebar navigation with role-based filtering
│   └── lib/
│       └── data.ts      # Temporary in-memory mock data for all entities
├── next.config.mjs
├── tailwind.config.ts
├── tsconfig.json
└── package.json
```

---

## 🔐 Role-Based Access

Change the `role` variable in `src/lib/data.ts` to simulate different user views:

```ts
// src/lib/data.ts
export let role = "admin"; // "admin" | "teacher" | "student" | "parent"
```

| Menu Item | admin | teacher | student | parent |
|---|:---:|:---:|:---:|:---:|
| Teachers / Students / Parents | ✅ | ✅ | ❌ | ❌ |
| Subjects | ✅ | ❌ | ❌ | ❌ |
| Classes / Lessons | ✅ | ✅ | ❌ | ❌ |
| Exams / Assignments / Results | ✅ | ✅ | ✅ | ✅ |
| Attendance / Events / Messages / Announcements | ✅ | ✅ | ✅ | ✅ |

---

## 🚀 Getting Started

**Prerequisites:** Node.js 18 LTS or later.

```bash
# 1. Clone the repository
git clone https://github.com/walidkuzi/SMS.git
cd SMS

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📜 Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start local dev server with HMR |
| `npm run build` | Production build |
| `npm run start` | Serve the production build |
| `npm run lint` | Run ESLint |

---

## 🙏 Acknowledgements

- [Lama Dev](https://youtube.com/lamadev) — original tutorial series
- [Next.js](https://nextjs.org/), [Tailwind CSS](https://tailwindcss.com/), [Pexels](https://www.pexels.com/) (placeholder images)