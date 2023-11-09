# Django 3 with PostgreSQL and Redis

*Spesification :*
- Linux Debian 11 (Bullseye)
- Python 3.11.4
- PostgreSQL 15.3
- Django 3.2.19
- Redis 7.2/latest


### Beberapa file yang perlu dikonfigurasi :
*Several files that needed to be configured :*

1. ./.env
2. ./requirements.txt
3. ./src/settings.py

### Menjalankan aplikasi Django pada Docker
*How to run docker django app*

1. Build docker image
```
docker-compose build
```
2. Run docker container
```
docker-compose up -d
```
3. Create database
```
docker-compose exec web python manage.py migrate
```
4. Create superuser
```
docker-compose exec web python manage.py createsuperuser
```
5. Collect static files
```
docker-compose exec web python manage.py collectstatic
```
6. Run django app
```
docker-compose exec web python manage.py runserver
```
7. Open browser and type the url addres : http://localhost or http://localhost:8080


That's it! & Good luck!<br>
by [mazjohn.com](https://mazjohn.com)

References: <br>
https://github.com/docker/awesome-compose/tree/master/official-documentation-samples/django