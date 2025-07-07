# 🐳 Docker Services for a Multi-Server Homelab

This repository contains Docker Compose configurations for individual containerized services used across multiple servers in a self-hosted homelab environment.

Each service (e.g., web apps, databases, networking tools) is configured to run independently, allowing for flexible deployment depending on the purpose of each server.

---

## 📁 Repository Structure

Each folder contains a single service with its own `docker-compose.yml` and optional `.env` file:

- `docker-services/`
  - `service-1/`
    - `docker-compose.yml`
    - `.env.example`
  - `service-2/`
    - `docker-compose.yml`
    - `.env.example`
  - `service-3/`
    - `docker-compose.yml`
  - `service-4/`
    - `docker-compose.yml`
  - `.gitignore`
  - `README.md`


## 🚀 How to Use

1. **Clone the repo on any Docker-enabled server:**
   ```bash
   git clone git@github.com:youruser/docker-stacks.git /opt/stacks
2. **Navigate to a service directory:**
   cd /opt/stacks/service-1
3. **(Optional) Copy and edit the .env file:**
   cp .env.example .env
4. **Start the service:**
   docker compose --env-file .env up -d

> 💡 Each server can run any combination of services. Nothing is hard-coupled.


## 🔒 Secrets & Environment Variables
Secrets like passwords and API keys are stored in .env files, which are excluded from Git using .gitignore. Each service includes a .env.example file showing the required variables.


## 📌 Tips
Keep services modular so each one can be updated or redeployed independently.

Use git pull && docker compose up -d to redeploy quickly.

Consider setting up watchtower for automatic image updates.


## 🛠 Tools Used

| Purpose            | Tool               |
|--------------------|--------------------|
| Container runtime  | Docker             |
| Orchestration      | Docker Compose     |
| Git versioning     | Git + GitHub       |
| Code editing       | Visual Studio Code |
| Mobile editing     | Textastic (iOS)    |
| Mobile Git         | Working Copy (iOS) |
