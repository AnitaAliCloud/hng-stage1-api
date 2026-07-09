# Personal API

A lightweight REST API built with Node.js and Express, containerized with Docker, and deployed on AWS EC2. Includes a GitHub Actions CI pipeline that automatically builds, scans, and pushes images to Amazon ECR on every push to `main`.

## Tech Stack

- Node.js / Express
- Docker (multi-stage build)
- AWS EC2 + Nginx + PM2
- GitHub Actions
- Amazon ECR
- Trivy (security scanning)

## Getting Started

### Run with Node.js

```bash
git clone https://github.com/AnitaAliCloud/hng-stage1-api.git
cd hng-stage1-api
npm install
node index.js
```

### Run with Docker

```bash
docker build --target production -t personal-api:local .
docker run -p 3000:3000 personal-api:local
```

The API will be available at `http://localhost:3000`

## Endpoints

| Method | Endpoint | Response |
|--------|----------|----------|
| GET | `/` | `{ "message": "API is running" }` |
| GET | `/health` | `{ "message": "healthy" }` |
| GET | `/me` | `{ "name", "email", "github" }` |

## CI/CD Pipeline

Every push to `main` triggers a GitHub Actions workflow that:
1. Builds the Docker image using a multi-stage Dockerfile
2. Scans the image for vulnerabilities with Trivy
3. Pushes the image to Amazon ECR with a semantic version tag

## Live Deployment

🌍 **Live API:** `devopsprod.duckdns.org`