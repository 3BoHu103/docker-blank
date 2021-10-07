<h3 align="center">Blank docker container - django gunicorn nginx postgresql</h3>

### Инструменты разработки
**Стек:**
- Python == 3.9.6-alpine
- DB == postgres:13.0-alpine
- Django == 3.2.8
- gunicorn==20.1.0


## Разработка с Docker
##### 1) Клонировать репозиторий
##### 3) настроить .env.dev и docer-compose.yml на свои данные
##### 4) создать образ и запустить контейнер (docker-compose -f docker-compose.yml up -d --build)
##### 5) docker-compose -f docker-compose.yml exec web python manage.py migrate --noinput - мигрировать
##### 6) docker-compose -f docker-compose.yml exec web python manage.py collectstatic --no-input --clear - собрать статику
##### 7) docker exec -it pysonet_pysonet_back_1 python manage.py createsuperuser - создать суперюзера

comment in entrypoint.sh:
- python manage.py flush --no-input
- python manage.py migrate




For deploy use:
docker-compose.prod.yml
