# 🧩 DevOps Project – Todo App

This project demonstrates a complete DevOps pipeline including Docker, GitHub Actions, Ansible, Docker Compose, Kubernetes, and ArgoCD.

---

## ✅ Part 1: Dockerize App & CI Pipeline

🔗 **Repo Cloned From:**  
https://github.com/Ankit6098/Todo-List-nodejs

🛠 **MongoDB Setup:**  
Configured the app to connect to a private MongoDB Atlas instance via a `.env` file (excluded via `.gitignore`).

🐳 **Dockerization:**  
A `Dockerfile` was created to containerize the app, exposing port `4000`.

🔄 **GitHub Actions CI:**  
A CI workflow builds and pushes the Docker image to Docker Hub (private) on each push to the `main` branch.

- **Secrets Used:** `DOCKER_USERNAME`, `DOCKER_PASSWORD`

---

## ✅ Part 2: Provision EC2 with Ansible

☁️ **VM Setup:**  
Created an AWS EC2 instance (Ubuntu 24.04).

⚙️ **Provisioning with Ansible (from local machine):**  
Installed the following:
- Docker  
- Git  
- System updates

---

## ✅ Part 3: Deploy with Docker Compose & Enable Auto Updates

🔧 **Deployment Overview:**  
The application was deployed to the EC2 instance using `docker-compose.yml`, with environment variables loaded from `.env`.

📈 **Health Check:**  
Configured inside `docker-compose.yml` to monitor the app's status.

🔄 **Auto Update with Watchtower:**  
Watchtower is included as a service to monitor the app container.  
When a new version of the image is pushed to Docker Hub, Watchtower:
- Pulls the latest image  
- Restarts the container automatically

🌐 **App Access:**  
The live Todo App is accessible at:  
`http://<EC2-PUBLIC-IP>:4000`

---

## 🚀 Part 4: GitOps with Kubernetes & ArgoCD

The final stage of this pipeline (Kubernetes deployment + Continuous Delivery with ArgoCD) is implemented in a separate repository:

🔗 https://github.com/Mhamaadd/todo-k8s

---
