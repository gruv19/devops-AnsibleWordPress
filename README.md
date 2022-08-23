# ПРАКТИКА ПО ANSIBLE

## Подготовка к запуску playbook
Сделать в каталоге с playbook файл secret_vars.yml, добавить в него переменные:
```yml
remote_username: <имя пользователя>
db_name: <имя базы данных>
db_user: <имя пользователя БД>
db_pass: <пароль пользователя БД>
```

## Запуск playbook
```bash
ansible-playbook /home/r_grushev/playbooks/wordpress.yml --ask-become-pass
```