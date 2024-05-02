### Описание

**Yatube** - это бэкенд для социальной сети, в которой люди могут делиться событиями из своей жизни: выкладывать посты, оставлять комментарии под постами других пользователей и подписываться на интересующие группы и пользователей.


### Стек технологий

Архитектура проекта - REST API

*Используемые фреймворки и библиотеки*:

- Django 3.2
- Django Rest Framework 3.12
- Pillow 9.3
- PyJWT 2.8
- Djoser 2.1


### Установка

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:Randy-Colt/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```


### Документация

Документация API доступна по адресу: `http://127.0.0.1:8000/redoc/`


### Примеры запросов

Получение публикаций:

*request:*
```
api/v1/posts/
```

*response:*
```
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```

Получение всех комментариев к публикации:

*request:*
```
api/v1/posts/{post_id}/comments/
```

*response:*
```
[
  {
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
  }
]
```
