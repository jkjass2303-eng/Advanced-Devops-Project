# Advanced DevOps Project

## Project Title
Production-Ready Multi-Container Application Deployment (Local Ubuntu Setup)

## Project Overview
This project demonstrates the deployment of a production-ready multi-container application using Docker Compose on Ubuntu. The setup includes a frontend service, backend API, MySQL database, and Nginx reverse proxy. The project also covers Linux administration, Git/GitHub workflows, Docker networking, monitoring, and production best practices.

---

## Technology Stack

- Ubuntu Linux
- Git & GitHub
- Docker
- Docker Compose
- Python Flask
- MySQL 8.4
- Nginx 1.27

---

## Project Structure

```text
advanced-devops-project/
│
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/
│   └── index.html
│
├── nginx/
│   └── default.conf
│
├── .env
├── docker-compose.yml
├── .gitignore
└── README.md
```

---

## Features

### Linux System Administration
- User management
- File permissions
- Docker group configuration
- Docker service management
- Firewall configuration using UFW

### Git & GitHub Workflow
- Main branch
- Develop branch
- Feature branches
- Pull Requests
- Version tagging
- Branch protection rules

### Multi-Container Architecture
- Frontend Container
- Backend API Container
- MySQL Database Container
- Nginx Reverse Proxy Container

### Docker Features
- Custom bridge network
- Named volumes
- Environment variables
- Restart policies
- Health checks

### Monitoring & Troubleshooting
- Docker logs
- Docker stats
- Network inspection
- Port inspection

---

## Docker Services

### Frontend
Serves static web content through Nginx.

### Backend
Flask-based REST API running on port 5000.

### Database
MySQL 8.4 database with persistent storage.

### Reverse Proxy
Nginx reverse proxy handling incoming requests.

---

## Environment Variables

Configured using a `.env` file.

Example:

```env
MYSQL_ROOT_PASSWORD=root123
MYSQL_DATABASE=devopsdb
```

---

## Docker Compose Deployment

Build and start containers:

```bash
docker compose up -d --build
```

Check running containers:

```bash
docker ps
```

View logs:

```bash
docker logs <container-name>
```

Stop containers:

```bash
docker compose down
```

---

## Networking

Custom Docker Bridge Network:

```text
devops-net
```

Services communicate internally using container names.

Example:

```text
backend -> mysql
nginx -> backend
```

---

## Data Persistence

Database data is stored using Docker named volumes.

Example:

```text
mysql-data
```

Data remains available after container restarts.

---

## Monitoring

View resource usage:

```bash
docker stats
```

Inspect networks:

```bash
docker network inspect devops-net
```

Check open ports:

```bash
ss -tulpn
```

---

## Production Best Practices

- Avoid using latest image tags
- Store credentials in environment variables
- Use named volumes for persistence
- Implement restart policies
- Monitor containers regularly
- Remove unused Docker resources

---

## Version

Current Release:

```text
v1.0
```

---

## Author

Jasmeet Kaur

DevOps Project – 2026
