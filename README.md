# Docker Portfolio — Rajat Pasi

A static HTML/CSS student portfolio for DevOps Practical 3 and 4.

## Files
- `index.html`: website structure
- `style.css`: website styling
- `Dockerfile`: Nginx Docker image instructions

## Requirements
- Git
- Docker Desktop (running)

## Clone
```bash
git clone https://github.com/YOUR_USERNAME/docker-portfolio.git
cd docker-portfolio
```
Replace `YOUR_USERNAME` with your GitHub username.

## Build and run
```bash
docker build -t portfolio .
docker run -d -p 8081:80 --name portfolio-container portfolio
docker ps
```
Open http://localhost:8081/ in a browser.

## Run again after editing files
```bash
docker rm -f portfolio-container
docker build -t portfolio .
docker run -d -p 8081:80 --name portfolio-container portfolio
```

## Jenkins Practical 4
Use the repository in a Jenkins pipeline. The build stage runs `docker build -t portfolio .`, the run stage recreates `portfolio-container`, and the verification stage runs `docker ps`. Jenkins needs permission to access the Docker engine.
