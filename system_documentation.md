# 📚 DevSkillsHub – A Developer Portfolio + Skill Tracker

## 🧭 Table of Contents
1. [Project Overview](#1-project-overview)  
2. [Features](#2-features)  
3. [Tech Stack](#3-tech-stack)  
4. [Folder Structure](#4-folder-structure)  
5. [Page Structure & Routes](#5-page-structure--routes)  
6. [Component Structure](#6-component-structure)  
7. [APIs and Integration](#7-apis-and-integration)  
8. [State Management](#8-state-management)  
9. [Styling](#9-styling)  
10. [Backend Functionality (Optional)](#10-backend-functionality-optional)  
11. [Chart Integration](#11-chart-integration)  
12. [Authentication (Optional)](#12-authentication-optional)  
13. [Form Validation](#13-form-validation)  
14. [Dark/Light Mode](#14-darklight-mode)  
15. [Deployment Guide](#15-deployment-guide)  
16. [Future Enhancements](#16-future-enhancements)

---

## 1. Project Overview

**DevSkillsHub** is a multi-functional personal portfolio that combines:

- A visually appealing, responsive developer portfolio
- A functional skill tracking dashboard for monitoring personal development
- Optional user accounts with data persistence and authentication

---

## 2. Features

### 🧩 Frontend:

- Multi-page SPA (React Router)
- Skills CRUD operations with proficiency ratings
- Progress notes with timestamps
- Charts showing skill growth
- Fetch projects dynamically from GitHub API
- Contact form with validation
- Dark/light mode toggle

### 🗂️ Backend (Optional):

- Firebase / Supabase / Node + MongoDB
- Login/Signup
- Save and retrieve skill data
- Multi-user support

---

## 3. Tech Stack

| Technology        | Purpose                                |
|------------------|----------------------------------------|
| React + Hooks     | Core Frontend Development              |
| React Router     | Page Routing                           |
| Axios            | API calls (GitHub, backend)            |
| Tailwind CSS     | Styling Framework                      |
| Chart.js / Recharts | Skill Progress Visualization         |
| Firebase / Supabase | Backend as a Service (optional)     |
| Node.js + MongoDB | Custom Backend Alternative (optional) |
| Vercel/Netlify   | Deployment                             |

---

## 4. Folder Structure

```
src/
├── assets/
├── components/
│   ├── Navbar.jsx
│   ├── Footer.jsx
│   ├── SkillCard.jsx
│   ├── ProjectCard.jsx
│   └── Charts/
├── pages/
│   ├── Home.jsx
│   ├── Projects.jsx
│   ├── Skills.jsx
│   ├── Contact.jsx
├── context/
│   ├── ThemeContext.jsx
│   └── AuthContext.jsx
├── services/
│   ├── githubAPI.js
│   └── firebaseService.js
├── App.jsx
├── index.js
└── App.css / tailwind.css
```

---

## 5. Page Structure & Routes

| Route          | Component         | Description                            |
|----------------|-------------------|----------------------------------------|
| `/`            | Home              | Hero section, intro, CTA               |
| `/projects`    | Projects          | Fetch and display GitHub projects      |
| `/skills`      | Skills            | Skill Tracker UI                       |
| `/contact`     | Contact           | Form with email submission/validation  |

---

## 6. Component Structure

### Common Components:

- `Navbar`: Dynamic links, theme toggle
- `Footer`: Contact info, links
- `ThemeToggle`: Button for switching themes

### Skills Page Components:

- `SkillForm`: Add/edit skill
- `SkillList`: List of skills
- `SkillCard`: Skill details, progress, delete
- `ProgressChart`: Renders chart.js/recharts graph

---

## 7. APIs and Integration

### 🔗 GitHub API:
- Use `GET https://api.github.com/users/{username}/repos`
- Fetch project name, description, URL, language

### 🔁 Axios:
- All external API interactions (GitHub, backend) through Axios

---

## 8. State Management

- React Hooks (`useState`, `useEffect`, `useContext`)
- For global states like dark mode or authenticated user, use `Context API`
- Persist skills using localStorage (or backend)

---

## 9. Styling

- **Tailwind CSS** (recommended for rapid styling)
- Optional: use Styled Components
- Responsive: Mobile-first design with utility classes
- Dark/light mode support with Tailwind’s `dark` variant

---

## 10. Backend Functionality (Optional)

Choose one backend option:

### Firebase:

- Firestore for saving skills
- Firebase Auth for login/signup
- Firebase Hosting (optional)

### Supabase:

- PostgreSQL DB
- Built-in Auth

### Node.js + MongoDB:

- Custom REST API
- CRUD endpoints for skills

---

## 11. Chart Integration

Use either:

- **Chart.js** or **Recharts**
- Line graph for skill progress over time
- Bar graph for proficiency comparison

### Example Chart Data Structure:

```js
[
  { date: '2025-01-01', skill: 'React', progress: 5 },
  { date: '2025-02-01', skill: 'React', progress: 7 },
]
```

---

## 12. Authentication (Optional)

### Firebase Auth:

- Email/Password login
- `useContext` to manage user session
- Route guards (e.g., `/skills` only after login)

---

## 13. Form Validation

Use `react-hook-form` or native validation:

- Name, email, and message fields required
- Email format validation
- Confirmation message/modal on submit

---

## 14. Dark/Light Mode

- `ThemeContext` with `useContext`
- Toggle button in Navbar
- Tailwind class toggling using `dark` mode strategy

---

## 15. Deployment Guide

- Host frontend on **Vercel** or **Netlify**
- Firebase backend auto-hosted (if used)
- For custom backend (Node.js), deploy on **Render**, **Railway**, or **Heroku**

---

## 16. Future Enhancements

- User avatars and profile customization
- Resume upload/download
- Export skills as CSV
- Admin panel for moderation (if multi-user)
- PWA support