# The Authors Blog Website - Backend

## Project Description

The Authors Blog Website is a comprehensive platform that allows users to create posts, like and comment on them, and manage their accounts through user registration, login, and logout functionalities. This repository contains the backend codebase for the platform.

## Features

- **Post Creation**: Users can create, edit, and delete blog posts.
- **Likes and Comments**: Users can like and comment on posts.
- **User Authentication**: Registration, login, and logout functionalities.
- **Asynchronous Tasks**: Background task management for sending emails and other operations.

## Technologies & Achievements

### Docker
- Deployed using multiple containers for different services:
  - **Django**: The web framework.
  - **PostgreSQL**: The database.
  - **Redis**: In-memory data structure store for Celery.
  - **Nginx**: Web server for serving static files and handling requests.

### Django & DRF (Django Rest Framework)
- Developed RESTful APIs with Class-Based Views for efficient CRUD operations.

### Security
- Secured APIs with HTTPS/SSL.
- Implemented token-based authentication to ensure secure access to the APIs.

### Asynchronous Tasks
- Managed asynchronous tasks with **Celery** and **Redis**.
- Monitored task execution via **Flower**.

### API Testing
- Used **Pytest** along with factories and fixtures for comprehensive testing of the APIs.

### Email Management
- Integrated **Mailhog** for email testing in the development environment.
- Used **Mailgun** for email management in the production environment.

### Static & Media Files
- Served static and media files efficiently with **Nginx** and **Whitenoise**.

### Automation
- Streamlined development workflows with Shell Scripting and Makefiles.

## Installation

### Prerequisites
- Docker
- Docker Compose

### Steps
1. Clone the repository:
    ```bash
    git clone https://github.com/Abenezer0923/-Authors-Blog.git
    cd the-authors-blog-backend
    ```
2. Build and start the Docker containers:
    ```bash
    docker-compose up --build
    ```
3. Apply the migrations:
    ```bash
    docker-compose exec web python manage.py migrate
    ```
4. Create a superuser for the Django admin:
    ```bash
    docker-compose exec web python manage.py createsuperuser
    ```

## Usage

- Access the application at `http://localhost`.
- Admin interface at `http://localhost/admin`.

## Testing

Run the tests using Pytest:
```bash
docker-compose exec web pytest
