# devops-todo-app  

This project is part of the DevOps Internship challenge.

## How to run

1. Build Docker image:
docker build -t todo-app .

2. Run Docker container:
docker run -p 4000:4000 todo-app

3. Open in browser:
http://localhost:4000

CI Pipeline
GitHub Actions workflow builds Docker image on every push to main branch.

Environment Variables
Uses .env file (excluded from repo) for sensitive data like MongoDB connection string.


This README will be updated as the project progresses.

---

