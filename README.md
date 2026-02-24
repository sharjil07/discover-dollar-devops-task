# Discover Dollar DevOps Assignment - MEAN CRUD App

## 📌 Project Overview
Successfully containerized and deployed a full-stack MEAN (MongoDB, Express, Angular 15, Node.js) application with a fully automated CI/CD pipeline.

## 🛠️ Tech Stack & Tools
- **Frontend:** Angular 15
- **Backend:** Node.js / Express
- **Database:** MongoDB 6 (Dockerized)
- **Proxy:** Nginx (Reverse Proxy)
- **CI/CD:** GitHub Actions
- **Cloud:** AWS EC2 (Ubuntu)

## 🐳 Containerization Details
- **Frontend Dockerfile:** Uses a multi-stage build. Stage 1 builds the Angular app, and Stage 2 serves it via Nginx.
- **Backend Dockerfile:** Uses Node 18 to serve the REST API on port 8080.
- **Nginx Config:** Configured to serve the frontend on `/` and proxy API requests to the backend on `/api/`.

## 🔄 CI/CD Pipeline
The GitHub Action (`deploy.yml`) performs the following on every push to `main`:
1. Logs into Docker Hub.
2. Builds and Pushes `sharjil07/crud-dd-frontend` and `sharjil07/crud-dd-backend`.
3. SSH into AWS EC2.
4. Pulls the latest images and restarts containers using `docker-compose up -d`.

## 🚀 How to Run Locally
1. Clone the repo.
2. Run `docker-compose up --build`.
3. Access the app at `http://localhost`.

## 📊 Deployment Screenshots

### 1. GitHub Repository Structure
!<img width="1223" height="665" alt="image" src="https://github.com/user-attachments/assets/542886eb-0176-455b-ab1b-39d7577912c4" />


### 2. Docker Hub Repositories
!<img width="1866" height="523" alt="image" src="https://github.com/user-attachments/assets/815ddf9a-ac31-4961-ba60-096fc8dbd492" />


### 3. AWS EC2 Instance & Security Groups
!<img width="1896" height="816" alt="image" src="https://github.com/user-attachments/assets/6716cc98-6ed7-4674-8426-c6bb58d458a5" />


### 4. Running Containers (docker ps)
<img width="1390" height="196" alt="image" src="https://github.com/user-attachments/assets/538ebef1-667f-48a0-8274-3f1e04a32914" />


### 5. Application UI (Live)
<img width="1457" height="815" alt="Screenshot 2026-02-24 022305" src="https://github.com/user-attachments/assets/508243ef-4fde-443b-97f7-e5b6df8de056" />


---
**Deployment Link:** http://[YOUR-EC2-PUBLIC-IP]
