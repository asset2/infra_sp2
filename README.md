# API YamDB

## Проект Django REST API.

### Описание

- Проект **YaMDb** собирает отзывы пользователей на произведения. Произведения делятся на категории: «Книги», «Фильмы», «Музыка».

### Запуск проекта

- Клонируем репозиторий и перейдем в него
```python
 git clone https://github.com/asset2/infra_sp2
 cd infra_sp2/
```

- Установите Docker (https://docs.docker.com/get-started/)

- Запуск приложения

```python
  docker-compose up -d --build
```

- Выполнить миграции и создание суперпользователя

```python
  docker-compose exec web python manage.py migrate --noinput
  docker-compose exec web python manage.py createsuperuser
```

- Заполнение базы начальными данными

```python
 docker-compose exec web python manage.py loaddata fixtures.json
```

Интструкция как пользоваться данным API доступна по адресу http://localhost/redoc/