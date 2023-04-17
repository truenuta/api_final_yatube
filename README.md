# Проект «API для Yatube»
Через интерфейс REST API для Yatube могут работать мобильные приложения или чат-бот;
Так же можно передавать данные в любое приложение или на фронтенд.

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/api_final_yatube.git
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

Запустить проект:

```
python3 manage.py runserver
```

## Примеры запросов

Получить список всех публикаций

```
http://127.0.0.1:8000/api/v1/posts/
```

Удаление публикации

```
http://127.0.0.1:8000/api/v1/posts/{id}/
```

Добавление нового комментария к публикации

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```

Получение комментария к публикации по id.

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
```
