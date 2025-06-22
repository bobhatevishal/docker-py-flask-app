# docker-py-flask-app
# 🚀 Flask Dockerized Web Server with Nginx Reverse Proxy

This project demonstrates how to containerize a simple Flask API using Docker and serve it via Nginx reverse proxy. It's a beginner-friendly microservice setup ideal for learning Docker networking and deployment.

---

## 🌐 Features

- A lightweight **Flask API** with routes:
  - `/` – Welcome message
  - `/quote` – Returns a random programming quote
  - `/json` – Returns a sample JSON response
- **Dockerfile** for building the Flask app container
- **Nginx** configured as a reverse proxy to route traffic to the Flask app
- Uses Docker **user-defined bridge network** for internal communication

---

## 🛠️ Tech Stack

- Python 3.9 (Slim)
- Flask 2.0.2
- Gunicorn (optional for production)
- Nginx
- Docker

---

## 📁 File Structure

├── app.py # Flask application
├── Dockerfile # Flask app Dockerfile
├── requirements.txt # Python dependencies
├── default.conf # Nginx configuration


---

## 🐳 Docker Commands

### 1️⃣ Build the Flask App Container:
```bash
docker build -t mypythonimg .
docker network create frontend
docker run -d --name myaap --network frontend mypythonimg

📌 Notes
Make sure to update the proxy_pass IP in default.conf based on your container's
internal IP or use container name if using Docker network.
This setup is ideal for local development, learning Docker networking,
and testing Flask microservices with a reverse proxy.
