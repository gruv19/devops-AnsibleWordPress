# ПРАКТИКА ПО ANSIBLE

## Требования
- Python v3.10.4;
- Ansible Core v2.12.0-1;
- Ansible v2.10.7;
- Убедиться, что в составле Ansible имеется модуль community.mysql.

## Подготовка к запуску playbook
Сделать в каталоге с playbook файл secret_vars.yml, добавить в него переменные:
```yml
remote_username: <имя пользователя>
db_name: <имя базы данных>
db_user: <имя пользователя БД>
db_pass: <пароль пользователя БД>
```

В этом каталоге создать файл inventory и добавить в него:
```
[webservers]
192.168.111.19
```

## Запуск playbook
```bash
ansible-playbook wordpress.yml -i inventory --ask-become-pass
```