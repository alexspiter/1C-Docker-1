# docker-1c-server

## Что это?

docker-1c-server -- это сервер 1С:Предприятия в контейнере Docker.

## Как это установить?

Для установки и начального запуска получите дистрибутив сервера 1С:Предприятия: https://users.v8.1c.ru/ -> Скачать обновления -> Технологическая платформа 8.3 -> ВЕРСИЯ -> Cервер 1С:Предприятия (64-bit) для DEB-based Linux-систем -> Скачать дистрибутив

Клонируйте репозиторий:

    git clone https://github.com/alexanderfefelov/docker-1c-server.git

Скопируйте deb-файлы дистрибутива сервера 1С:Предприятия в каталог `docker-1c-server` и затем выполните команды:

    cd docker-1c-server
    ./build.sh
    ./run.sh

## Как остановить/запустить/перезапустить контейнер?

Для управления контейнером используйте команды:

    docker stop docker-1c-server
    docker start docker-1c-server
    docker restart docker-1c-server

## Где мои данные?

Данные сервера 1С:Предприятия вы можете найти в каталогах `/var/lib/docker/volumes/1c-server-home/_data` (домашний каталог пользователя `usr1cv8`) и `/var/lib/docker/volumes/1c-server-logs/_data` (технологические журналы).
