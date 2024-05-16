# devops-thiio

# Dockerized Laravel Application with Nginx, MySQL, and Random HTTP Service

This project sets up a Docker environment for a Laravel application with Nginx as the web server, MySQL as the database, and optionally includes a random HTTP Docker service. The Laravel application retrieves data from the MySQL database and responds to requests, while Nginx routes traffic to the appropriate services.

## Setup Instructions

### Prerequisites

- Docker Engine: Install Docker according to your operating system instructions [here](https://docs.docker.com/get-docker/).
- Docker Compose: Ensure Docker Compose is installed. It typically comes bundled with Docker Desktop.

### Getting Started

1. Clone this repository:

   ```bash
   git clone <https://github.com/geraalmaguerr/devops-thiio.git>
   cd <repository-directory>

2. Build and start the Docker containers:

    docker-compose up --build

    Add --profile random if you want to include the optional random HTTP Docker service.\

3. Access the Laravel application in your browser at http://localhost:8000.

4. Access the Nginx server status page at http://localhost/nginx_status.

## Environment Configuration

# Laravel Application:

Environment variables for the database connection are configured in the docker-compose.yml file under the laravel service.
Additional Laravel configuration can be done within the Laravel application files.

# Nginx Server:

Nginx configuration can be modified in the nginx/nginx.conf file.
Server blocks for routing requests are defined in the Nginx configuration.

# MySQL Database:

MySQL configuration is set in the docker-compose.yml file under the mysql service.
Additional MySQL configuration can be done through environment variables.

# Random HTTP Docker Service (Optional):

Configuration for the random HTTP Docker service can be done in the docker-compose.yml file under the random_http service.

## Running Tests
Tests for the Laravel application can be executed within the Laravel container. Follow these steps:

1. Access the Laravel container:
    docker-compose exec laravel bash

2. Run tests using PHPUnit:
    php artisan test

## Additional Notes

    If you encounter any issues, refer to the Docker logs for each service.
    For advanced configurations or troubleshooting, consult the Docker and Laravel documentation.

