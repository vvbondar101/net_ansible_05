# Домашнее задание к занятию 5 «Тестирование roles
## Molecule

Запуск molecule test -s centos_7 внутри корневой директории clickhouse-role.
![molecule test](/images/molecule01.png)


Создание сценария тестирования по умолчанию при помощи molecule init scenario --driver-name docker.
![molecule 02](/images/molecule02.png)

Добавление нескольких разных дистрибутивов (centos:8, ubuntu:latest) для инстансов
![molecule 03](/images/molecule03.png)

Добавление нескольких assert в verify.yml-файл для проверки работоспособности vector-role и запуск тестирования роли повторно
![molecule 05](/images/molecule05.png)

## TOX

Запуск docker run --privileged=True -v <path_to_repo>:/opt/vector-role -w /opt/vector-role -it aragast/netology:latest /bin/bash. Выполнение команды tox внутри контейнера.
![tox 01](/images/tox01.png)

Создание облегчённого сценария для molecule с драйвером molecule_podman. Проверка его на исполнимость.
![tox 02](/images/tox02.png)

Правильная команда в tox.ini, чтобы запускался облегчённый сценарий.
![tox 03](/images/tox03.png)

Запуск команды tox.
![tox 04](/images/tox04.png)