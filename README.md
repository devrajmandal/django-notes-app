# Notes App — Django + Nginx + MySQL

A containerized notes application built with React and Django,
deployed on AWS EC2 using Docker, Nginx reverse proxy, and MySQL.

---

## Architecture

<img width="1105" height="683" alt="Architecture" src="https://github.com/user-attachments/assets/d4e999f2-3dde-496f-b94f-1a3d4df04d07" />

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Django (Python) |
| Frontend | React |
| Database | MySQL with persistent volume |
| Reverse Proxy | Nginx |
| Deployment | Docker, Docker Compose, AWS EC2 |

---

## Requirements

- Docker
- Docker Compose

---

## Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/devrajmandal/django-notes-app.git
cd django-notes-app
```

### 2. Build and run all containers
```bash
docker compose up -d
```

This starts three containers:

| Container | Port | Role |
|-----------|------|------|
| Nginx | 80 | Reverse proxy |
| Django | 8000 | App server |
| MySQL | 3306 | Database |

### 3. Access the app

Open `http://<your-ec2-ip>/` in your browser

---

## Project Structure
```
├── Dockerfile
├── docker-compose.yml
├── nginx/
│   └── default.conf
├── mynotes/          # Django app
└── requirements.txt
```

---

## Screenshots

**App**
<img width="1919" height="940" alt="app_screenshot" src="https://github.com/user-attachments/assets/05c2ab5d-a3d4-4a79-9c51-bf756de7afcc" />

**Containers running**
<img width="1919" height="689" alt="terminal" src="https://github.com/user-attachments/assets/3f417c9c-8e34-4820-80d5-068cd308bfce" />

**EC2 Instance**
<img width="1919" height="864" alt="ec2-instance" src="https://github.com/user-attachments/assets/553d5de1-90c3-496c-9d30-0c3400b56e26" />
