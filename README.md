<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README</title>
</head>
<body>
    <h1>The Authors Blog Website - Backend</h1>

    <h2>Project Description</h2>
    <p>The Authors Blog Website is a comprehensive platform that allows users to create posts, like and comment on them, and manage their accounts through user registration, login, and logout functionalities. This repository contains the backend codebase for the platform.</p>

    <h2>Features</h2>
    <ul>
        <li><strong>Post Creation</strong>: Users can create, edit, and delete blog posts.</li>
        <li><strong>Likes and Comments</strong>: Users can like and comment on posts.</li>
        <li><strong>User Authentication</strong>: Registration, login, and logout functionalities.</li>
        <li><strong>Asynchronous Tasks</strong>: Background task management for sending emails and other operations.</li>
    </ul>

    <h2>Technologies & Achievements</h2>

    <h3>Docker</h3>
    <p>Deployed using multiple containers for different services:</p>
    <ul>
        <li><strong>Django</strong>: The web framework.</li>
        <li><strong>PostgreSQL</strong>: The database.</li>
        <li><strong>Redis</strong>: In-memory data structure store for Celery.</li>
        <li><strong>Nginx</strong>: Web server for serving static files and handling requests.</li>
    </ul>

    <h3>Django & DRF (Django Rest Framework)</h3>
    <p>Developed RESTful APIs with Class-Based Views for efficient CRUD operations.</p>

    <h3>Security</h3>
    <ul>
        <li>Secured APIs with HTTPS/SSL.</li>
        <li>Implemented token-based authentication to ensure secure access to the APIs.</li>
    </ul>

    <h3>Asynchronous Tasks</h3>
    <p>Managed asynchronous tasks with <strong>Celery</strong> and <strong>Redis</strong>. Monitored task execution via <strong>Flower</strong>.</p>

    <h3>API Testing</h3>
    <p>Used <strong>Pytest</strong> along with factories and fixtures for comprehensive testing of the APIs.</p>

    <h3>Email Management</h3>
    <p>Integrated <strong>Mailhog</strong> for email testing in the development environment. Used <strong>Mailgun</strong> for email management in the production environment.</p>

    <h3>Static & Media Files</h3>
    <p>Served static and media files efficiently with <strong>Nginx</strong> and <strong>Whitenoise</strong>.</p>

    <h3>Automation</h3>
    <p>Streamlined development workflows with Shell Scripting and Makefiles.</p>

    <h2>Installation</h2>

    <h3>Prerequisites</h3>
    <ul>
        <li>Docker</li>
        <li>Docker Compose</li>
    </ul>

    <h3>Steps</h3>
    <ol>
        <li>Clone the repository:
            <pre><code>git clone https://github.com/yourusername/the-authors-blog-backend.git
cd the-authors-blog-backend</code></pre>
        </li>
        <li>Build and start the Docker containers:
            <pre><code>docker-compose up --build</code></pre>
        </li>
        <li>Apply the migrations:
            <pre><code>docker-compose exec web python manage.py migrate</code></pre>
        </li>
        <li>Create a superuser for the Django admin:
            <pre><code>docker-compose exec web python manage.py createsuperuser</code></pre>
        </li>
    </ol>

    <h2>Usage</h2>
    <ul>
        <li>Access the application at <code>http://localhost</code>.</li>
        <li>Admin interface at <code>http://localhost/admin</code>.</li>
    </ul>

    <h2>Testing</h2>
    <p>Run the tests using Pytest:
        <pre><code>docker-compose exec web pytest</code></pre>
    </p>

    <h2>Contributing</h2>
    <p>Contributions are welcome! Please open an issue or submit a pull request.</p>

    <h2>License</h2>
    <p>This project is licensed under the MIT License. See the <a href="LICENSE">LICENSE</a> file for details.</p>
</body>
</html>
