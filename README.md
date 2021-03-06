## Шаблон Docker-обвязки для любого PHP-приложения
Включает в себя PHP, MySQL, PHPMyAdmin и Caddyserver 2. Можно использовать как development-среде, так и  в production.

### Предварительные соглашения:
1. Предполагается, что все ваши проекты хранятся в папке `$HOME/code`.
2. На компьютере установлен [Docker](https://docs.docker.com/get-docker/) и [Docker-Compose](https://docs.docker.com/compose/install/).

### Скачай
1. Скачай в папку `$HOME/code` этот репозиторий.
2. Переименуй папку под свой проект.

### Сконфигурируй
1. Создай копию файла `.env.template` и назови копию `.env`. Пропиши в этом файле текущее окружение (`dev` или `prod`. Для машины разработчика `dev`), пароль к БД и абсолютный путь до своего php-проекта.
2. В файле `/etc/hosts` добавь запись
```
127.0.0.1       mysite.test
127.0.0.1       db.test
```

### Запусти
1. Находясь в папке проекта запусти команду `docker-compose up -d` - она сбилдит и запустит контейнеры.

### Let's code not war
Сайт доступен по адресу [mysite.test](http://mysite.test), а phpmyadmin по адресу [db.test](http://db.test)


### Послесловие
* Для запуска контейнеров в фоновом режиме, выполни в корне проекта команду `docker-compose up -d`.
* Для остановки контейнеров выполни в корне проекта команду `docker-compose down`.


### Статья по настройке XDebug 3
https://region23.dev/all/xdebug-3-docker-vs-code/
