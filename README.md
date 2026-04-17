🐳 Docker Practice Repository
📌 Overview

This repository is created to practice and understand Docker fundamentals and advanced concepts. It includes examples, commands, and mini-projects to help in learning containerization effectively.

Docker helps developers package applications with all dependencies into a standardized unit called a container, ensuring consistency across different environments.

🎯 Objectives
Understand Docker architecture and working
Learn how to create and manage containers
Build custom Docker images using Dockerfile
Work with Docker Hub and image repositories
Practice container networking and volumes
Run real-world applications using Docker
🛠️ Technologies Used
Docker
Docker CLI
Docker Hub
Linux Commands
Node.js / Python (for sample apps)
📂 Project Structure
docker-practice/
│
├── app/                  # Sample application
│   ├── index.js
│   ├── package.json
│
├── Dockerfile            # Docker image configuration
├── docker-compose.yml    # Multi-container setup
├── .dockerignore         # Ignore unnecessary files
└── README.md             # Project documentation
⚙️ Prerequisites

Make sure you have installed:

Docker Desktop (Mac/Windows)
OR Docker Engine (Linux)

Check installation:

docker --version
🚀 Getting Started
1. Clone Repository
git clone https://github.com/your-username/docker-practice.git
cd docker-practice
2. Build Docker Image
docker build -t docker-practice-app .
3. Run Container
docker run -d -p 3000:3000 docker-practice-app

Open in browser:

http://localhost:3000
📦 Docker Commands Cheat Sheet
🔹 Basic Commands
docker pull nginx
docker images
docker ps
docker ps -a
docker run nginx
docker stop <container_id>
docker rm <container_id>
docker rmi <image_id>
🔹 Build & Run
docker build -t my-app .
docker run -p 3000:3000 my-app
🔹 Logs & Exec
docker logs <container_id>
docker exec -it <container_id> bash
🧱 Dockerfile Example
# Base image
FROM node:18

# Set working directory
WORKDIR /app

# Copy files
COPY package.json .
RUN npm install

COPY . .

# Expose port
EXPOSE 3000

# Start app
CMD ["npm", "start"]
🔗 Docker Compose Example
version: '3'
services:
  web:
    build: .
    ports:
      - "3000:3000"

Run:

docker-compose up
📊 Key Concepts Covered
Images vs Containers
Dockerfile
Volumes
Networks
Docker Compose
Port Mapping
Environment Variables
📁 .dockerignore Example
node_modules
npm-debug.log
.git
.gitignore
🌐 Use Cases
Microservices architecture
CI/CD pipelines
Cloud deployment
Development environment consistency
🧠 Learning Outcomes

After completing this practice, you will be able to:

Build and deploy containerized applications
Debug container issues
Optimize Docker images
Use Docker in real-world projects
🤝 Contributing

Feel free to fork this repository and add your own Docker experiments.

📜 License

This project is for educational purposes.

⭐ Acknowledgement

Inspired by real-world DevOps practices and Docker documentation.
