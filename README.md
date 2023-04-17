# Проект «API для Yatube»
Через интерфейс REST API для Yatube могут работать мобильные приложения или чат-бот;
Так же можно передавать данные в любое приложение или на фронтенд.

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:truenuta/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

## Примеры запросов

#### Получить список всех публикаций

```
http://127.0.0.1:8000/api/v1/posts/
```
Пример ответа в формате json:

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

#### Удаление публикации

```
http://127.0.0.1:8000/api/v1/posts/{id}/
```
Пример ответа в формате json:

```
{
  "detail": "Учетные данные не были предоставлены."
}
```

#### Добавление нового комментария к публикации

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```

Пример ответа в формате json:

```
{
  "text": "string"
}
```

#### Получение комментария к публикации по id.

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
```

Пример ответа в формате json:

```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}

```
