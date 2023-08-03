# Django Oscar Template

Для запуска проекта потребуется `solr` реализуемый в `docker-compose.yml`:

```bash
docker compose up
```

В данный момент для запуска необходимо создать переменную окружения хряняющую
`SECRET_KEY` следующим образом:

 - Windows:
```bash 
setx DJANGO_SECRET_KEY "ваш_секретный_ключ"
```

 - Linux/macOS:
```bash
export DJANGO_SECRET_KEY="ваш_секретный_ключ"
```

## Установка зависимостей

Находясь в корневой директории проекта? используй команду, чтобы установить необхоидмые зависимости python:

```bash
pip install -r requirements.txt
```

Далее перейди в папку `/source` и примени миграции:

```bash
cd source
python manage.py migrate
```

Создай супер-пользователя:

```bash
python manage.py createsuperuser
```

И запусти сервер:

```bash
python manage.py runserver
```

# Дальнейшие планы

- Запуск проекта через докер,
- Использование postgresql в качестве основной базы,
- Изменение шаблонов под собственный лад,
- И многое другое о чем я пока не хочу думать или не догадываюсь.