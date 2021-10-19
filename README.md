# Задание
![image](https://user-images.githubusercontent.com/72396348/137326383-b395fc8e-d8f2-4de0-9721-5e607729377a.png)

# Установка
- Склонировать репозиторий https://github.com/Stevinel/test_outofcloud
- Установить виртуальное окружение python -m venv venv
- Выполнить команды:
   ```
   docker-compose up -d --build
   docker-compose exec web python manage.py migrate --noinput
   docker-compose exec web python manage.py createsuperuser
   docker-compose exec web python manage.py collectstatic --no-input
   ```
- Зайти в Postman для тестирования
- Отправить POST запрос по эндпойнту http://127.0.0.1/api/v1/emails/ с ключом email
- Можно смотреть созданные данные в админке http://127.0.0.1/admin/ 

# Стек
- Python
- Django
- Docker
- Nginx
- Gunicorn
- Postgresql
