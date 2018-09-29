# Содержание
Содержит контейнер БД (postgres) и контейнер с api, который работает c mqtt broker 

# Репозиторий с кодом (laravel)
https://github.com/yyyyeeeeesss/flespi-laravel

Docker контейнер с postgres содержит 20 000 нагенерированных данных пользователей.  

# Запуск сервиса dbs через docker

1. Скачать репозиторий
2. В папке проекта из командной строки выплнить docker-compose up -d 
3. В файле docker-compose.yml в переменную MQTT_TOKEN - указать токен к flespi.io
4. Выполнить docker-compose exec php /usr/bin/php /var/flespi/artisan bus:listen
5. Открыть https://codepen.io/yyyyeeeeesss/pen/PdrdYW и вначале js файла указать токен с шага 3

В итоге должно работать примерно так:
![teamwork-flip](https://im2.ezgif.com/tmp/ezgif-2-fe2896dc74.gif)