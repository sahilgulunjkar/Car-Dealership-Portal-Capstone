# Full Stack Capstone - Car Dealership Portal

Welcome to the Car Dealership Portal! This is a full-stack application that allows users to view dealerships, browse cars, and submit reviews with automated sentiment analysis.

## 🚀 Tech Stack

- **Frontend:** React.js
- **Backend:** Django (Python)
- **Database & Microservices:** Node.js, Express, MongoDB
- **Containerization:** Docker & Docker Compose

## ✨ Features

- **User Authentication:** Sign up, log in, and log out functionalities.
- **Dealership Directory:** Browse all dealerships or filter by state.
- **Dealer Details:** View detailed information about a specific dealership and its reviews.
- **Review System:** Authenticated users can post reviews for dealerships.
- **Sentiment Analysis:** Reviews are automatically analyzed for their sentiment (positive, neutral, negative).

## 🛠️ Project Structure

- `/server/frontend`: React application.
- `/server/djangoapp`: Django backend application containing the core logic, views, and models.
- `/server/database`: Node.js microservice connected to MongoDB for handling dealership and review data. Containerized with Docker.
- `/start_dev.ps1`: An automated PowerShell script to spin up the entire development environment in one click!

## 🏃‍♂️ How to Run the Application

### The Easy Way (Windows / PowerShell)

We have provided a comprehensive startup script that automates the entire process, including starting Docker, building images, running database containers, starting the Django server, and launching the React frontend.

Just open PowerShell as Administrator and run:
```powershell
.\start_dev.ps1
```

### The Manual Way

If you prefer to start the services manually, follow these steps:

#### 1. Database & Microservice (Docker)
Open a terminal and navigate to the database directory:
```bash
cd server/database
docker build . -t nodeapp
docker-compose up -d
```

#### 2. Django Backend
Open a new terminal, activate the virtual environment, and run the server:
```bash
cd server
..\dgangoenv\Scripts\activate
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```
*Note: The backend runs on `http://localhost:8000`*

#### 3. React Frontend
Open a new terminal and start the React app:
```bash
cd server/frontend
npm install
npm start
```
*Note: The frontend runs on `http://localhost:3000`*

## � Screenshots

### Home Page
![Home Page](screenshots/Home%20Page.png)

### Review Dealers Page
![Review Dealers Page](screenshots/Review%20Dealers%20Page.png)
