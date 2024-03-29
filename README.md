## Проект «API для Yatube»

### Описание проекта:

Програмный интерфейс для социальной сети Yatube, по средствам которого 
пользователи могут публиковать свои записи, редактировать и удалять их. 
Также можно просматривать контент других пользователей, оставлять к ним 
коментарии и подписываться на понравившихся им пользователей.

Всем пользователям доступен контент других пользователей для просмотра. 
Для создания своего контента необходимо пройти аутентификацию. 
Аутентификация с помощью JWT-токена.

### Стек технологий:
<img src="https://img.shields.io/badge/Python-FFFFFF?style=for-the-badge&logo=python&logoColor=3776AB"/><img src="https://img.shields.io/badge/django-FFFFFF?style=for-the-badge&logo=django&logoColor=082E08"/><img src="https://img.shields.io/badge/Django REST Framework-FFFFFF?style=for-the-badge&logo=&logoColor=361508"/><img src="https://img.shields.io/badge/SQLite-FFFFFF?style=for-the-badge&logo=SQLite&logoColor=003B57"/>

### Как запустить проект:

##### Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Excellent-84/api_final_yatube.git
cd api_final_yatube
```

##### Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
source venv/bin/activate
python3 -m pip install --upgrade pip
```

##### Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

##### Создать файл .env и указать необходимые токены по примеру .env.example:
``` 
touch .env
```

##### Выполнить миграции:

```
cd yatube_api
python3 manage.py migrate
```

##### Запустить проект:

```
python3 manage.py runserver
```


### Примеры запросов к API:

##### Получение публикаций:

Метод GET к эндпоинту   http://127.0.0.1:8000/api/v1/posts/{id}/

Пример ответа:

```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}
```

##### Создание публикации:

Метод POST к эндпоинту   http://127.0.0.1:8000/api/v1/posts/

```
{
  "text": "string",
  "image": "string",
  "group": 0
}
```

Пример ответа:

```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}
```

##### Подробную версию запросов можно посмотреть по адресу: http://127.0.0.1:8000/redoc/

#### Автор: [Горин Евгений](https://github.com/Excellent-84)
