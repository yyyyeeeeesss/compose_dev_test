# Содержание
Содержит контейнер БД (postgres) и контейнер с приложением, которое работает c mqtt broker 

# Репозиторий с кодом (laravel)
https://github.com/yyyyeeeeesss/flespi-laravel

# Запуск сервиса dbs через docker

1. Скачать репозиторий
2. В папке проекта из командной строки выплнить docker-compose up -d 
3. В файле docker-compose.yml в переменную MQTT_TOKEN - указать токен к flespi.io
4. Выполнить docker-compose exec php /usr/bin/php /var/flespi/artisan migrate (нужно немного подождать, будет сгенерировано 10 000 пользователей)
5. Выполнить docker-compose exec php /usr/bin/php /var/flespi/artisan bus:listen
6. Открыть https://codepen.io/yyyyeeeeesss/pen/PdrdYW и вначале js файла указать токен из шага 3

В итоге должно работать примерно так:
https://youtu.be/04F9aHSIEhA
