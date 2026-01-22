
RCA Management System

Project Overview
The RCA (Root Cause Analysis) Management System is a lightweight web application used to log incidents and perform root cause analysis for each incident.

The system is built using a frontend-only HTML/CSS/JavaScript approach with PocketBase as the backend and database.
The entire solution is containerized using Docker and Docker Compose.

Architecture 
Browser (HTML + CSS + JS)
        |
        | REST API (fetch)
        v
PocketBase Backend (Docker)
        |
     SQLite Database
     
Technology Stack
Layer                  Technology
Frontend            HTML, CSS, JavaScript
Backend             PocketBase
Database            SQLite (PocketBase default)
Deployment          Docker, Docker Compose

Folder Architecture – RCA Management System
RCA-MANAGEMENT-SYSTEM/
│
├── frontend/
│   ├── index.html        # Complete frontend (HTML + CSS + JS in ONE file)
│   └── Dockerfile        # Frontend Docker image (Nginx)
│
├── pocketbase/
│   └── pb_data/          # PocketBase database (auto-generated)
│
├── docker-compose.yml    # Runs frontend + PocketBase together
│
└── README.md             # Project documentation 

Implementation Steps
Step 1: Open CMD in PocketBase folder
Step 2: Run PocketBase
./pocketbase serve
Output should look like:
Server started at http://127.0.0.1:8090
Admin UI: http://127.0.0.1:8090/_/
Open Admin UI:
http://localhost:8090/_/
Step 3: Open terminal in vscode 
Where docker-compose.yml exists.
 Step 4: Start containers
docker compose up -d
Step 5: Verify container
docker ps
Step 6:Run index.html

Conclusion 
This project demonstrates a modern, lightweight, and containerized approach to building a full-stack application using REST APIs and backend-as-a-service architecture.
It is easy to deploy, maintain, and extend, making it suitable for demos, learning, and internal tools.

It is:
Easy to deploy
Easy to maintain
Easy to extend


