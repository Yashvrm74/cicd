
# 🚀 CI/CD Pipeline Demo (Node.js + Docker + GitHub Actions)

This project demonstrates a complete CI/CD pipeline setup for a Node.js application using:

- 🐙 GitHub Actions for CI/CD automation
- 🐳 Docker for containerization
- 📦 Docker Hub for image hosting
- 💻 Local deployment (no cloud needed)

---

## 📁 Project Structure

```
.
├── app.js                  # Node.js Express app
├── Dockerfile              # Docker image build instructions
├── docker-compose.yml      # Local dev setup
├── package.json            # NPM scripts and dependencies
└── .github/workflows/
    └── ci-cd.yml           # CI/CD workflow
```

---

## 🧪 How CI/CD Works

On every `push` or `pull request` to the `main` branch:

1. ✅ Code is checked out
2. 🧪 Tests are run using `npm test`
3. 🛠️ Docker image is built
4. 📤 Image is pushed to Docker Hub

### 🔧 GitHub Actions Workflow

The CI/CD pipeline uses:
- `docker/login-action`
- `docker/build-push-action`
- GitHub secrets for Docker Hub credentials

---

## 🐳 How to Run the App Locally

Make sure Docker is running on your system.

### 📥 Pull and Run the Docker Image

```bash
docker run -d -p 3000:3000 yashvrm74/cicd-pipeline-demo:latest
```

Then visit: [http://localhost:3000](http://localhost:3000)

You should see:
```
CI/CD Pipeline is working!
```

---

## 📷 Screenshots

- ✅ GitHub Actions Workflow Passing  
- ✅ Docker Hub Image  
- ✅ App Running in Browser  
- ✅ Docker Container Running (`docker ps`)
