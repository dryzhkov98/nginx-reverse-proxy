# Nginx Reverse Proxy

Настройка Nginx как обратного прокси с помощью Docker Compose. Конфигурация предназначена для проксирования запросов к API серверу.

## Перед запуском
Перед началом работы убедитесь, потребуются следующие компоненты:
- Docker: [Установка Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Установка Docker Compose](https://docs.docker.com/compose/install/)

## Настройка


1. Склонируйте репозиторий:

   ```bash
   git clone https://github.com/yourusername/nginx-reverse-proxy.git
   ```

2. Cкопируйте переменные окружения и присвойте им значения

    ```.dotenv
     TZ=Europe/Moscow
     NGINX_PORT=80
     NGINX_UPSTREAM=api-backend
     NGINX_UPSTREAM_PORT=3000
    ```

3. Перейдите в корневую директорию проекта и запустите Docker Compose:
    ```bash
      docker-compose up -d
    ```

## Настройка Nginx
Ваш конфигурационный файл Nginx (nginx.conf) находится в корне проекта. Вы можете настроить его по своим потребностям.

## Логи
Логи Nginx доступны в директории ./logs.

## Пользовательские шаблоны
Вы можете добавлять пользовательские шаблоны конфигурации Nginx в директорию ./templates и затем использовать их в вашем конфигурационном файле Nginx.

## Примечание
По умолчанию, проект использует образ nginx:stable-alpine из Docker Hub. Вы можете изменить его в файле docker-compose.yml.
