# Документация проекта yatube_final_api
 <br>
 API проекта Yatube.<br>
 <br>
 Доступные эндпоинты: <br>
 'api/v1/posts/'<br>
 'api/v1/groups/'<br>
 'api/v1/posts/post_id/comments/'<br>
 'api/v1/follow/'<br>
 Эндпоинт для работы с токенами:<br>
 'api/v1/jwt/create/' - получить токен<br>
 'api/v1/jwt/refresh/' - обновить токен<br>
 'api/v1/jwt/verify/' - проверить токен<br>
 <br>
 
 ## Установка проекта: 
 Клонируйте репозиторий,
 
 Установите виртуальное окружение командой **```python -m venv venv```**
 
 Активируйте виртуальное окружение командой **```venv/Scripts/activate```**
 
 Установите зависимости **```pip install -r requirements.txt```**
 
 Выполните миграции **```python manage.py migrate```**
 
 Запустите проект **```python manage.py runserver```**
 
 ## **Примеры запросов**<br>
 GET запрос  http://127.0.0.1:8000/api/v1/posts/{id}/<br>
  <br>
  Выведет информацию о посте с выбранным id<br>
{<br>
 "id": 0,<br>
 "author": "string",<br>
 "text": "string",<br>
 "pub_date": "2019-08-24T14:15:22Z",<br>
 "image": "string",<br>
 "group": 0<br>
}<br>
 <br>
 POST запрос http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/<br>
 Добавит комментарий к выбранному посту<br>
 <br>
{<br>
"text": "string"<br>
}<br>
<br>
GET запрос http://127.0.0.1:8000/api/v1/follow/<br>
<br>
Выведет информацию о ваших подписках<br>
<br>
[{<br>
"user": "string",<br>
"following": "string"<br>
}]<br>
<br>
 
