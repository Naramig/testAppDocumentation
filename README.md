# Test App Documentation

Эта документация описывает бэкенд для сервиса заметок

## Сервисы

### Сервис пользователей [github](#https://github.com/Naramig/users-api) 
Сервис имеет регистрацию и авторизацию (JWT). Также есть возможность удалить и изменить созданные данные.
При запуске сервиса, создается учетка админа. Админ имеет полный CRUD пользователей, а также возможность давать права админа другим пользователям.
При создании нового пользователя создается сообщение в Kafka на отправку приветственного письма.

### Сервис записей [github](#https://github.com/Naramig/notion-api)
Сервис имеет CRUD заметок. Авторизация через JWT

### Сервис рассылки E-mail уведомлений [github](#https://github.com/Naramig/email-api)
Сервис обрабатывает сообщения из Kafka и отправляет email.

## Local run
Для локального запуска можно использовать docker compose файл, который находится в этом репозитории.
Актуальные имеджи сервисов будут скачиваться с docker hub. (Github Action использовался для CI/CD)

### Useful Commands:

```$ docker compose up ``` - Builds, (re)creates, starts, and attaches to containers for a service.

```$ docker compose -f [path]/[docker-compose].yml up``` - Specify an alternate compose file

(When the command exits, all containers are stopped.)

```$ docker compose up -d``` - Starts the containers in the background and leaves them running

### Postman
Для удобного тестирования можно импортировать коллекцию для Postman (Postman/TestApp.postman_collection.json)

### Swagger
В сервисах в папке swagger есть файл index.html который откроет автоматизированную документацию
TODO - улучшить автогенерацию

### Дополнительную информация по сервисам находится в README сервисов