# LEMP stack + flask, mongodb docker-compose

## Setup /etc/hosts/

127.0.0.1 its.flask
127.0.0.1 its.php

## Service
nginx:latest
python:3.6
mongo:4.0.8
php:8
mysql:8
phpmyadmin:5

## Setup mongodb
`docker exec -it mongodb bash` password: quang12345
`use flaskdb` - switch to flaskdb
`db.createUser({user: 'quangtran', pwd: 'quang12345', roles: [{role: 'readWrite', db: 'flaskdb'}]})`
`exit`
`exit`
## Usage
dockker-compose up -d
go to "http://its.flask/todo" for request todo app