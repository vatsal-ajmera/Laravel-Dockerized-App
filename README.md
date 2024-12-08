FOR vertual host:
in this case we have used docker-app.local host, which is registered in xampp folder with their folder name.

- docker-compose exec -it app sh : use this command to enter in to command shall to run artisan commands

- docker exec -it mysql-container  bash : use this command to enter in to mysql container shall to run Msql Queries
- mysql -u <username> -p : after run above command, this command will used to connect to mysql

- docker-compose down - to remove all images
- docker-compose up -d - to create new images

-docker logs mysql-container - to print logs of specified containers <mysql-container> is mysql container name


use this ref: https://dev.to/kamruzzaman/dockerizing-a-laravel-app-nginx-mysql-phpmyadmin-and-php-82-43ne




Clone the repository.
cp .env.example .env
Start the Docker containers: docker-compose up -d
Install dependencies: docker exec -it laravel_app composer install
Run database migrations: docker exec -it laravel_app php artisan migrate
