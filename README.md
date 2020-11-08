<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

# Description

[This](https://github.com/jjuanrivvera99/laravel-nginx-mysql-docker) is a complete laravel environment using docker-compose with the following services: nginx, queue daemon, redis, mysql, scheduler and node js.

## How to run this project

To run this project you need to have docker and docker-compose installed in your machine.

Take the following steps:

- clone this repository by executing the following command: 'git clone https://github.com/jjuanrivvera99/laravel-nginx-mysql-docker'
- change directory: 'cd laravel-nginx-mysql-docker'
- run command: 'docker-compose pull'
- run command: 'docker-compose up -d'
- run command: 'docker-compose exec app setup'
- run command: 'docker-compose exec app permissions'
- run command: 'docker-compose exec app fix'

Enable auth (Laravel 6+):

- run command: docker-compose exec app composer install laravel/ui
- run command: docker-compose exec app php artisan ui vue --auth
- run command: docker-compose exec node npm install
- run command: docker-compose exec node npm run dev

## License

The Laravel framework is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).
