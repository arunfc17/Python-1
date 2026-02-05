# End-to-End DevOps CI/CD Pipeline Demo

## 🚀 Project Overview
This repository demonstrates a real DevOps CI/CD workflow:
- Jenkins builds a Docker image from the source code
- The container runs a Python application automatically
- All steps are version-controlled and reproducible

## 📦 Tools Used
- Git & GitHub (Version Control)
- Jenkins (CI/CD Orchestration)
- Docker (Containerization)
- Python Flask (Application)

## 🔁 Pipeline Flow
1. Developer pushes code to GitHub
2. Jenkins triggers pipeline
3. Docker image is built
4. Container runs the Python Flask app

## ⚠️ Challenges & Fixes
### 🔹 Docker Port Conflicts
- Containers sometimes failed due to port 5000 already in use
- Fixed by removing old containers before running new ones

### 🔹 Jenkins Pipeline Errors
- Initial pipeline failures due to permission issues
- Fixed using proper Docker permissions for Jenkins

## 🧪 How To Run Locally
1. Clone repo
2. Build image:
```bash
docker build -t python-devops-app .
