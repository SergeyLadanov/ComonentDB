# Пример работы с MySQL на Python

## Установка необходимых компоненты

### Установка python
Python (https://www.python.org)
### Установка модулей для работы с базой данных mySQL
```
pip install peewee
pip install cryptography
pip install PyMySQL
```

### Установка модулей для WEB приложения

```
pip install flask
pip install cherrypy
```
### Установка mysql сервера
Инструкция на сайте: https://www.mysql.com

## Подготовка базы данных
### Создание БД
Запуск консоли mysql:
```
mysql -u root -p
```
Далее необходимо ввести пароль, который был указан при установке mysql.

Создается база:
```
CREATE DATABASE db_name;
```
Создание пользователя и привилегий для использования БД:
```
GRANT ALL PRIVILEGES ON db_name.* TO 'user_name'@'localhost' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;
```
Выход
```
exit
```

### Настройки после создания БД
Для указанных настроек БД соответствтующий раздел файла config.py будет выглядеть так:
```
#----Database settings----#
# Host for mySQL database
DB_HOST = "localhost"
# User of database
DB_USER = "user_name"
# Name of database
DB_NAME = "db_name"
# Password for database
DB_PSWD = "password"

```
