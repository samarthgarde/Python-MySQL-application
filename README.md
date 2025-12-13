# Python-MySQL-application

This project is a simple Flask-based web application with MySQL database integration, fully containerized using Docker.
It supports user signup, signin, and dashboard functionality and demonstrates real-world backend + DevOps concepts.

## 🚀 Features

User Signup & Signin

Session-based authentication

MySQL database for storing user data

Dockerized Flask application

## 🛠️ Tech Stack

- **Backend**: Python, Flask

- **Database**: MySQL 8

- **Containerization**: Docker

## 📂 Project Structure

'''
Python-MySQL-application/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── templates/
│   ├── signup.html
│   ├── signin.html
│   └── dashboard.html
└── README.md
'''

## 🐬 MySQL Setup (Docker)

Run MySQL container:

docker run -d \
  --name mysql-db \
  -e MYSQL_ROOT_PASSWORD=rootpass \
  -e MYSQL_DATABASE=database-1 \
  -e MYSQL_USER=admin \
  -e MYSQL_PASSWORD=adminpass \
  mysql:8.0

## 🐳 Build Flask Application Image
'''docker build -t python-mysql-app .'''

## ▶️ Run Flask Application
'''
docker run -d \
  --name signup-app \
  --link mysql-db \
  -p 5000:5000 \
  python-mysql-app
'''

## 🌐 Access the Application

Open your browser:

http://localhost:5000/signup

## ⭐ If you like this project

Give it a ⭐ on GitHub!