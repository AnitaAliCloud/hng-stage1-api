# HNG DevOps Stage 1 — Personal API

A simple REST API built with Node.js and Express, deployed on a VPS with Nginx reverse proxy.

## How to Run Locally
1. Clone the repository: git clone https://github.com/anitaalicloud/hng-stage1-api.git cd hng-stage1-api
2. Install dependencies: npm install
3. Start the server: node index.js
4. API runs at http://localhost:3000

## Endpoints

| Endpoint | Response |
|---|---|
| GET / | {"message":"API is running"} |
| GET /health | {"message":"healthy"} |
| GET /me | {"name":"Ali Anita Onyinye","email":"anitaali496@gmail.com","github":"https://github.com/anitaalicloud"} |

## Live URl
https://anitaalicloud.duckdns.org
