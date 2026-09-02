# GitPulse — GitHub Audience Tracker
[🚀 Live Demo](https://git-pulse-nine.vercel.app/)

GitPulse is a full-stack GitHub audience tracking application that monitors followers and following activity over time.

The application connects to the GitHub REST API, collects follower and following data, stores snapshots in MongoDB, and detects changes between syncs. This makes it possible to track current followers, following activity, and followers who have been lost.

---

## 🚀 Features

- Track GitHub followers
- Track GitHub following
- Synchronize GitHub data on demand
- Store follower snapshots in MongoDB
- Detect follower changes between syncs
- Maintain a history of follower events
- View current followers
- View current following
- Identify lost followers
- View follower history
- Automatically synchronize data using GitHub Actions
- Interactive web dashboard

---

## 🏗️ How It Works

GitPulse follows this data flow:

GitHub Account  
↓  
GitHub REST API  
↓  
FastAPI Backend  
↓  
MongoDB Atlas  
↓  
Next.js Frontend  
↓  
GitPulse Dashboard

During a sync, GitPulse fetches the latest follower and following information from GitHub.

The application compares the new data with previously stored information in MongoDB and records changes as events.

This allows the application to maintain a historical record instead of only showing the current follower count.

---

## 🛠️ Technologies Used

### Backend

- Python
- FastAPI
- Uvicorn
- PyMongo
- Requests
- Python-dotenv
- APScheduler

### Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS

### Database

- MongoDB
- MongoDB Atlas

### APIs & Automation

- GitHub REST API
- GitHub Actions

### Deployment

- Render — Backend
- Vercel — Frontend
- MongoDB Atlas — Database

---

## 📁 Project Structure

```text
GitPulse/
│
├── backend/
│   ├── app/
│   ├── scripts/
│   ├── .env.example
│   ├── Dockerfile
│   └── requirements.txt
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── app/
│   │   ├── components/
│   │   └── lib/
│   ├── package.json
│   └── package-lock.json
│
├── .github/
│   └── workflows/
│
├── .gitignore
└── README.md
