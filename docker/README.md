# TDD in Laravel

## Steps to build laravel on docker

```sh
$ git clone git@github.com:arihito/LaravelTDD.git
$ cd LaravelTDD/docker

# LaravelTDD
# ├── app
# └── docker

$ cp .env.example .env
$ docker-compose up -d
$ docker exec -it laravel-tdd_app_1 ash

> composer create-project --prefer-dist "laravel/laravel" .
> exit

$ cd ../app
$ php artisan serve
# 127.0.0.1:8000
```

## Make command on Docker alias

- For windows, [pass](https://beyondjapan.com/blog/2020/10/makefile-docker/) the environment variable path of the 'make command'.
- Mac can be executed as it is.

### Run


Run the following command in docker directory.

```sh
$ make up
```

Open `http://localhost` in a browser.

### Stop

Run the following command in docker directory.

```sh
$ make stop
```

### Down

Stop and delete all docker images and all running containers.

```sh
$ make down
```
