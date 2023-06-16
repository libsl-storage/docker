# docker

Docker-compose файл для деплоя libsl-storage.

## Порядок запуска:
- Скачать docker-compose.yml
- Создать .env-файл в одной директории с docker-compose.yml, указать в нём следующие переменные окружения:
  - DB_URL: ссылка до базы данных в формате jdbc:postgresql://HOSTMANE:PORT/DB
  - DB_USERNAME: логин БД
  - DB_PASSWORD: пароль БД
  - SECURITY_KEY: 256-bit ключ безопасности
  - SUPERUSER_NAME: имя суперпользователя проекта
  - SUPERUSER_EMAIL: почта суперпользователя проекта
  - SUPERUSER_PASSWORD: пароль суперпользователя проекта
  - VUE_APP_ROOT_API: ссылка к backend'у в формате http://HOSTNAME:PORT
  - ALLOWED_ORIGINS: перечисление хостов, из которых возможен доступ к backend'у в формате http://HOSTNAME:PORT,http://HOSTNAME:PORT...
- Выполнить docker-compose up
