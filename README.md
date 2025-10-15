# Hospital Management System

A full-stack web application for managing core hospital operations. This project features a Spring Boot backend API and a React frontend, with a focus on CI/CD best practices using Docker for deployment.

## Tech Stack

* **Backend:** Java, Spring Boot, Maven
* **Frontend:** React (Vite), JavaScript, CSS
* **Database:** MySQL
* **Deployment:** Docker, Nginx

## Prerequisites

Before you begin, ensure you have the following installed:
* Git
* Java (JDK 17 or later)
* Maven
* Node.js (v18 or later) & npm
* MySQL Server
* Docker

## How to Run Locally

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)<YOUR_USERNAME>/hospital-management-system.git
    cd hospital-management-system
    ```

2.  **Setup the Database:**
    * Log in to MySQL and create the database:
        ```sql
        CREATE DATABASE hospital;
        ```

3.  **Run the Backend:**
    * Navigate to the backend directory and start the server.
    ```bash
    cd hospital-backend
    mvn spring-boot:run
    ```
    * The API will be available at `http://localhost:8081`.

4.  **Run the Frontend:**
    * Open a **new terminal** and navigate to the frontend directory.
    ```bash
    cd hospital-frontend
    npm install
    npm run dev
    ```
    * The application will be available at `http://localhost:5173`.

## Frontend Deployment with Docker

The frontend is configured to be served via an Nginx container.

1.  **Navigate to the frontend directory:**
    ```bash
    cd hospital-frontend
    ```

2.  **Build the Docker image:**
    ```bash
    docker build -t hospital-frontend .
    ```

3.  **Run the Docker container:**
    ```bash
    docker run -d -p 80:80 --name hospital-frontend-container hospital-frontend
    ```
    The application will now be running on `http://localhost`.


