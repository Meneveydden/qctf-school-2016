
DoubleHash
======

Описание
---------
Участнику выдается файл (server(for users).py), это копия файла login_controllers, в котором звездочками закрыты флаг и соль (количество символов совпадает). Пользователь по комментарию в коде должен понять, что база данных сервиса открыта для анонимного доступа на чтение и, получив к ней доступ, попробовать подобрать соль, зарегистрировав пользователя с известным паролем. Перебрав все возможные соли (соль содержит 4 символа) пользователь найдет соль, после чего ему останется подобрать пароль от администратора. По комментарию пользователь должен догадаться, что пароль словарный, и перебрать какой-нибудь словарик. Найдя пароль пользователь логинится под админом и получает флаг.


Формулировка
---------
Кажется, этот сервис(ссылка) скрывает какую-то секретную информацию, но все, что нам удалось достать, это вот этот код(ссылка).


Файлы:
-----
1. **db_create.py** -- скрипт для создания таблицы в базе данных
2. **run.py** -- скрипт для запуска сервиса
3. **config.py** -- файл, хранящий connection_string
4. **app/login_controller.py** -- файл с сервисом
5. **server(for users).py** -- файл, который будет предоставлен пользователям (копия предыдущего, со звездочками)
6. **models.py** -- файл, в котором определена модель для базы данных
7. **templates/...** -- html templates.

Инструкция по запуску сервиса:
1. Заполнить правильно соединение с sql базой данных (не забыть открыть анонимный доступ ТОЛЬКО на чтение).
2. После запуска сервиса зарегистрировать аккаунт admin с каким-нибудь словарным паролем (или автоматизировать его регистрацию каким-либо образом).
3. Убедиться, что сервис доступен из интернета.


Flag: QCTF_cfc0fd7bf6aa8dede9f22dc1d9747323
=======
