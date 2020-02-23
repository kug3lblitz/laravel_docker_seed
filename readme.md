# laravel local development with docker
I found the setup processs for laravel in docker to be fairly easy to get wrong, so I made this for myself and others who don't necessarily want to run an entire lamp stack or install composer/apache on their local machine.

1) $ sh composer.sh create-project --prefer-dist laravel/laravel example-proj
2) edit config files, esp docker-compose.yml as needed for project
3) $ docker-compose pull
4) $ docker-compose build --force-rm
5) $ docker-compose up
6) optional:
    $ docker exec -it [container id] sh (for interactive shell, use of artisan)
