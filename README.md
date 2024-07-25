#  Как работать с репозиторием финального задания

## Что нужно сделать

Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.

# О проекте:
## Данный проект является разработкой REST приложения упакованного в Docker контейнеры.

## Автор проекта:
### GitHub [SkullPiercer](https://github.com/)

## Использованные технологии:
```python
  Django==3.2.16
```
```python
  djangorestframework==3.12.4
```
```python
  Docker
```
```python
  Nginx
```

# Как запустить проект.
### **Клонировать репозиторий и перейти в него в командной строке:**
```python 
  git clone git@github.com:SkullPiercer/kittygram_final.git
```
```python
  cd kittygram_final/kittygram_backend
```
### **Cоздать и активировать виртуальное окружение:**
#### Windows:
```python
  python -m venv venv
```
```python
  source venv/Scripts/activate
```
#### Linux/Mac:
```python
  python3 -m venv env
```
```python
  source env/bin/activate
```
### **Установить зависимости из файла requirements.txt:**
#### Windows:
```python
  python -m pip install --upgrade pip
```
```python
  pip install -r requirements.txt
```
#### Linux/Mac
```python
  python3 -m pip install --upgrade pip
```
```python
  pip install -r requirements.txt
```
### **Выполнить миграции:**
#### Windows:
```python
  python manage.py migrate
```
#### Linux/Mac
```python
  python3 manage.py migrate
```
### **Запустить проект:**
#### Windows:
```python
  python manage.py runserver
```
#### Linux/Mac:
```python
  python3 manage.py runserver
```

# Примеры запросов.
### **Эндпоинт /api/**
```python 
  Вернет вам информацию о доступных эндпоинтах
```
### **Эндпоинт /cats/**
```python 
  Вернет вам список котов
```