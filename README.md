# devops-thiio

# Dockerized Laravel Application with Nginx and MySQL

This project sets up a Docker environment for a Laravel application with Nginx as the web server and MySQL as the database. Additionally, it optionally includes a random HTTP Docker image service.

## Setup Instructions

### Prerequisites

Make sure you have Docker and Docker Compose installed on your system.

### Getting Started

1. Clone this repository:

   ```bash
   git clone <https://github.com/geraalmaguerr/devops-thiio.git>
   cd <repository-directory>

2. Build and start the Docker containers:

    docker-compose up --build

    Add --profile random if you want to include the optional random HTTP Docker image service.

3. Access the Laravel application in your browser at http://localhost:8000.

4. Access the Nginx server status page at http://localhost/nginx_status.

# Configuration

Laravel application:

Environment variables for database connection can be configured in the docker-compose.yml file under the laravel service.
Additional Laravel configuration can be done within the Laravel application files.
Nginx server:

Nginx configuration can be modified in the nginx/nginx.conf file.
Server blocks for routing requests are defined in the Nginx configuration.
MySQL database:

MySQL configuration is set in the docker-compose.yml file under the mysql service.
Additional MySQL configuration can be done through environment variables.
Random HTTP Docker image (optional):

Configuration for the random HTTP Docker image can be done in the docker-compose.yml file under the random_http service.

