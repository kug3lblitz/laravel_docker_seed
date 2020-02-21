# laravel local development with docker
I found the setup processs for laravel in docker to be fairly easy to get wrong, so I made this for myself and others who don't necessarily want to run an entire lamp stack or install composer/apache on their local machine.

1) $ git clone https://github.com/laravel/laravel.git laravel-app
2) $ docker run --rm -v $(pwd):/app composer install
3) $ mkdir -p nginx/conf.d
4) $ mv vhost.conf nginx/conf.d/ (may require sudo)
5) $ cp .env.example .env
6) $ docker-compose exec app php artisan key:generate
7) $ docker-compose exec app php artisan db:migrate --seed (if migrations are needed)
8) $ docker-compose up
9) profit
