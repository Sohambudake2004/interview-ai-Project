#  AI-Powered Job Preparation Platform

A full-stack GenAI web application that helps users prepare for job interviews by analyzing their resume against job descriptions, detecting skill gaps, generating personalized interview questions, and creating ATS-optimized resumes.

---

##  Features

-  **Secure Authentication** — JWT with token blacklisting, OTP email verification, httpOnly cookies
-  **Resume Upload & Parsing** — Upload resume and job description for AI analysis
-  **Skill Gap Detection** — Gemini AI detects missing skills based on JD vs resume
-  **Interview Question Generation** — Role-specific technical and behavioural questions
-  **Personalized Prep Plan** — Structured preparation plan based on detected gaps
-  **ATS Resume Generation** — Puppeteer-based dynamic PDF resume tailored to the job

---

##  Tech Stack

### Frontend
| Tech | Purpose |
|---|---|
| React.js + Vite | UI framework |
| React Router | Client-side routing |
| Axios | HTTP requests |
| Context API | Global state management |
| SCSS | Styling |

### Backend
| Tech | Purpose |
|---|---|
| Node.js + Express.js | Server & API |
| MongoDB + Mongoose | Database |
| JWT | Authentication |
| bcrypt | Password hashing |
| cookie-parser | Cookie management |
| Gemini AI | AI features |
| Puppeteer | PDF generation |

---

##  Project Structure

```
GenAI/
├── Backend/
│   ├── src/
│   │   ├── controllers/                 # auth.controller.js , interview.controller.js
│   │   ├── models/                      # user.model.js, blacklist.model.js, report.model.js
│   │   ├── routes/                      # auth.route.js, interview.route.js
│   │   ├── middlewares/                 # auth.middleware.js, file.middleware.js 
│   │   ├── config/                      # database.js
│   │   ├── services/                    # ai.service.js
│   │   └── app.js
│   ├── .env                             # Never committed
│   ├── .gitignore
│   ├── package.json
│   └── server.js
├── Frontend/
│   ├── src/
│   │   ├── features/
│   │   │   ├── auth/
│   │   │   │   ├── components           # Protected.jsx
│   │   │   │   ├── hooks/               # useAuth.jsx
│   │   │   │   ├── pages/               # Login.jsx, Register.jsx
│   │   │   │   ├── styles/              # auth.form.scss
│   │   │   │   ├── services/            # auth.api.jsx
│   │   │   │   └── auth.context.jsx
│   │   │   └── interview/
│   │   │       ├── components           
│   │   │       ├── hooks/               # useInterview.jsx
│   │   │       ├── pages/               # Home.jsx, Interview.jsx
│   │   │       ├── styles/              # home.scss, interview.scss
│   │   │       ├── services/            # interview.api.jsx
│   │   │       └── interview.context.jsx
│   │   ├── styles/                      # button.scss
│   │   ├── App.jsx
│   │   ├── style.scss
│   │   └── main.jsx
│   ├── index.html
│   └── package.json
└── README.md
```


