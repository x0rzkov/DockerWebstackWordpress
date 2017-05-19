README
======

Set up a full stack Wordpress environnement with docker

The docker-compose.yml works with:

* [Wordpress](https://github.com/docker-library/wordpress) (latest)
* [Nginx](https://github.com/nginxinc/docker-nginx) (latest)
* PHP-FPM (7.1)
* [Varnish](https://github.com/million12/docker-varnish) (latest)
* [Memcached](https://github.com/docker-library/memcached) (latest)
* [MariaDB](https://github.com/docker-library/mariadb) (latest)
* [phpMyAdmin](https://github.com/phpmyadmin/docker) (latest)
* [cadvisor](https://github.com/google/cadvisor) (latest)

Requirements
------------

Docker and docker compose

Installation
------------

    git clone https://github.com/crashbtz/DockerWebstackWordpress
    cd DockerWebstackWordpress
    docker-compose build
    docker-compose up


[http://localhost](http://localhost)

[http://localhost:8082](http://localhost:8082) => phpMyAdmin

[http://localhost:8081](http://localhost:8081) => Monitoring containers with [cadvisor](https://github.com/google/cadvisor)
