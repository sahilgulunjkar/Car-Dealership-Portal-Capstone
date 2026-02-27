# Full-Stack Car Dealership Platform

A comprehensive full-stack application for managing car dealerships, reviews, and inventory. This project utilizes a modern microservices architecture, combining a Django backend with a React frontend and a dedicated Node.js/MongoDB service for data management.

## 🏗️ System Architecture

The application is built using a decoupled architecture:
- **Backend (Django)**: Handles core application logic, user authentication, and serves the frontend static files.
- **Frontend (React)**: Provides a dynamic, responsive user interface for browsing dealers and posting reviews.
- **Database Service (Node.js/Express)**: A microservice that interacts with a MongoDB database to manage dealership and review data.
- **Sentiment Analysis**: An integrated feature that analyzes customer reviews to provide insights into sentiment.

## 🚀 Key Features

- **User Authentication**: Secure sign-up and login functionality.
- **Dealer Management**: Browse dealerships filtered by state or view individual dealer details.
- **Review System**: View reviews from other customers and post new reviews with car details.
- **Sentiment Insights**: Automatically analyzes the sentiment of posted reviews.
- **Inventory Search**: Integrated car inventory search functionality.

## 🛠️ Technology Stack

| Component | Technology |
| :--- | :--- |
| **Backend** | Python, Django, Django REST Framework |
| **Frontend** | JavaScript, React, React Router, HTML5, CSS3 |
| **Microservice** | Node.js, Express.js |
| **Databases** | SQLite (Django/Users), MongoDB (Dealerships/Reviews) |
| **Containerization** | Docker, Docker Compose |

## 📦 Installation & Setup

### Prerequisites
- Python 3.x
- Node.js & npm
- Docker Desktop

### Standard Setup

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd Full-Stack-Capstone
   ```

2. **Backend Setup**:
   - Create a virtual environment: `python -m venv dgangoenv`
   - Activate it: `.\dgangoenv\Scripts\activate`
   - Install dependencies: `pip install -r server/requirements.txt`
   - Run migrations: `python server/manage.py migrate`

3. **Frontend Setup**:
   - Navigate to `server/frontend`
   - Install dependencies: `npm install`
   - Build the project: `npm run build`

4. **Database Service Setup**:
   - Navigate to `server/database`
   - Follow the Docker instructions below or run manually with `npm install` and `node app.js`.

### 🐳 Docker Deployment (Recommended)

To deploy the application using Docker:

1. **Ensure Docker is running**.
2. **Start the services**:
   ```bash
   docker-compose up --build
   ```
   This command builds the images and starts the Django app, React frontend, and MongoDB service concurrently.

## 📂 Project Structure

- `server/`: Root of the Django backend and overall project logic.
  - `djangoapp/`: Core Django application logic and APIs.
  - `djangoproj/`: Django project settings and routing.
  - `frontend/`: React source code and build files.
  - `database/`: Node.js microservice for MongoDB interaction.
- `dgangoenv/`: Python virtual environment.
- `Screenshots/`: Application preview images.

## 📄 License

This project is licensed under the [MIT License](LICENSE).
