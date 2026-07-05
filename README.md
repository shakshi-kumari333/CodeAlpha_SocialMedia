# CodeAlpha_SocialMedia 👥


A mini full-stack Social Media Platform built for the **CodeAlp
Internship — Task 2**.


## ✨ Features
- User registration & login (JWT auth, hashed passwords)
- User profiles with editable bio
- Create, view, and delete posts
- Like / unlike posts
- Comment on posts
- Follow / unfollow other users
- Search for people by name


## 🛠 Tech Stack
- **Frontend:** HTML, CSS, JavaScript (vanilla)
- **Backend:** Node.js, Express.js
- **Database:** A lightweight JSON-file store (`social.json`) —
works instantly on any OS
- **Auth:** JWT stored in an HTTP-only cookie


## 📁 Project Structure
```
CodeAlpha_SocialMedia/
├── backend/
│   ├── config/db.js          # JSON-file database helper
│   ├── middleware/auth.js    # JWT auth middleware
│   ├── routes/                # auth, posts, users
│   ├── server.js              # Express app entry point
│   ├── seed.js                # Seeds demo users & posts
│   └── package.json
└── frontend/
    ├── index.html               # Feed (view + create posts)
    ├── profile.html              # User profile (bio, posts, f
    ├── people.html                # Search & follow users
    ├── login.html / register.html
    ├── css/style.css
    └── js/api.js, posts.js
```


## 🚀 How to Run


1. **Install dependencies**
   ```bash
   cd backend
   npm install
   ```


2. **Seed demo data** (creates 3 demo users + sample posts)
   ```bash
   node seed.js
   ```


3. **Start the server**
   ```bash
   npm start
   ```


4. Open your browser at **http://localhost:5001**
   (The Express server serves the frontend directly, so no sepa
needed.)


**Demo login:** `aisha@example.com` / `password123` (same passw
users — check `seed.js` for the other emails)


## 🔌 API Endpoints


| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login |
| POST | `/api/auth/logout` | Logout |
| GET | `/api/posts` | Get feed (supports `?userId=` to filter)
| POST | `/api/posts` | Create a post |
| DELETE | `/api/posts/:id` | Delete your own post |
| POST | `/api/posts/:id/like` | Toggle like on a post |
| GET | `/api/posts/:id/comments` | Get comments for a post |
| POST | `/api/posts/:id/comments` | Add a comment |
| GET | `/api/users` | Search users (supports `?search=`) |
| GET | `/api/users/:id` | Get a user's profile |
| PUT | `/api/users/me` | Update your own name/bio |
| POST | `/api/users/:id/follow` | Toggle follow on a user |


## 📌 Notes
- Database file (`social.json`) is created automatically on fir
- This project fulfills CodeAlpha Task 2 requirements: user pro
like/follow system.


---
Built as part of the **CodeAlpha Full Stack Development Interns

