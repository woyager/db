[![Build Status](https://travis-ci.org/woyager/db.svg?branch=master)](https://travis-ci.org/woyager/db)

DB Infra
=========

Установка и настройка Mongodb для приложения reddit в рамках курса "DevOps практики и инструменты".

Требования
----------

* Ubuntu 16.04

Role Variables
--------------

* mongo_bind_ip, mongo_port адрес и порт, на котором будет доступна mongodb
* env окружение, выводится при запуске роли в информационных целях

Tags
----

* install подключение репозитария и установка mongodb 3.2
* configure конфигурация (включение mongo_bind_ip, mongo_port в mongod.conf)

Example Playbook
----------------

    - hosts: dbserver
      roles:
        - {role: db, mongo_bind_ip: 10.0.0.2, mongo_port: 27018, env: staging}

