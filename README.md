# Ultimate Todo App 2025 🚀  
**The most powerful 100% FREE todo app you can deploy in 60 seconds**

Live Demo → https://todo-app-2tlb.onrender.com (your version will have its own URL)

https://user-images.githubusercontent.com/1676403/284961122-9f8c6c6c-1f2d-4e0b-9f8c-7d8f8f8f8f8f.gif

### Features (Everything works on the free tier)

- Multi-user login / register (secure bcrypt)
- Add, complete, delete, search todos
- Due dates with overdue / today / future badges
- Tags & categories (multi-select + custom colors)
- Full calendar view (FullCalendar)
- Dark mode (auto-saved)
- Email reminders 24h before due (via Resend – 3 000 free emails/mo)
- Progressive Web App – installable on phone & desktop
- 100% free forever on Render + free Postgres + free email

### Deploy in 60 Seconds (Zero Cost)

1. Click “Use this template” or fork this repo
2. Go to https://dashboard.render.com
3. New → Web Service → connect your repo → Free plan → Create
4. New → PostgreSQL → Free → Create → copy **Internal Database URL**
5. In your Web Service → Environment → add these 4 variables:

| Key              | Value                                                        |
|------------------|--------------------------------------------------------------|
| `DATABASE_URL`   | (paste the Internal Database URL from step 4)                |
| `SECRET_KEY`     | `any-long-random-string-2025`                                |
| `RESEND_API_KEY` | get free at https://resend.com → API Keys                    |
| `APP_URL`        | your Render URL (e.g. `https://todo-app-2tlb.onrender.com`)  |

6. (Optional but recommended) New → Background Worker → Command: `python scheduler.py` → same 4 env vars

Done! Your app is live forever for $0.

### File Structure
ultimate-todo-app/
├── app.py              → Main Flask app (all routes)
├── models.py           → SQLAlchemy models (User, Todo, Tag)
├── scheduler.py        → Daily email reminder worker
├── requirements.txt    → Exact dependencies
├── render.yaml         → Render.com config (free tier)
├── Procfile            → Legacy start command
├── runtime.txt         → Forces Python 3.11
├── static/
│   ├── style.css       → Dark mode + responsive design
│   ├── script.js       → Dark mode toggle + PWA
│   └── manifest.json   → Makes it installable
├── templates/
│   ├── base.html
│   ├── index.html      → Todo list + search
│   ├── calendar.html   → FullCalendar view
│   ├── login.html
│   └── register.html
└── utils/
└── email.py        → Resend email sender

Tech Stack

Flask 3 + Flask-Login + Flask-SQLAlchemy
PostgreSQL (Render free tier)
Gunicorn
Resend.com (free email)
FullCalendar.js
Pure HTML/CSS/JS (no React/Vue)

Credits
Built with ❤️ by you & Grok (xAI) in December 2025
Inspired by every todo app that ever charged money.
⭐ Star this repo if you love free powerful apps!
