# Dockerized Laravel Application

This repository demonstrates how to set up a Laravel application using Docker, complete with Nginx, MySQL, and PHPMyAdmin.

## Prerequisites

- Docker and Docker Compose installed on your system.
- XAMPP for managing local virtual hosts (if applicable).
- A registered virtual host, e.g., `docker-app.local`, in your XAMPP configuration folder.

## Getting Started

### Clone the Repository
```bash
git clone https://github.com/vatsal-ajmera/Laravel-Dockerized-App.git
cd Laravel-Dockerized-App
```

### Set Up Environment Variables
Copy the example `.env` file and configure it as needed:
```bash
cp .env.example .env
```

### Start the Docker Containers
Start the containers in detached mode:
```bash
docker-compose up -d
```

### Install Dependencies
Install Laravel dependencies using Composer:
```bash
docker exec -it app composer install
```

### Run Database Migrations
Run the migrations to set up your database schema:
```bash
docker exec -it app php artisan migrate
```

## Useful Commands

### Accessing the Laravel Application Container
Enter the application container shell to run Artisan commands:
```bash
docker-compose exec app sh
```

### Accessing the MySQL Container
Enter the MySQL container shell to run MySQL queries:
```bash
docker exec -it mysql-container bash
```

Once inside the MySQL shell, connect to the database using:
```bash
mysql -u root -p
```

### Stopping and Restarting Containers
Stop and remove all containers:
```bash
docker-compose down
```

Rebuild and start the containers:
```bash
docker-compose up -d
```

### Viewing Logs
View logs for a specific container (e.g., MySQL):
```bash
docker logs mysql-container
```

## Additional Reference
For more detailed guidance, refer to the following article: [Dockerizing a Laravel App](https://dev.to/kamruzzaman/dockerizing-a-laravel-app-nginx-mysql-phpmyadmin-and-php-82-43ne)

---

Happy coding!
