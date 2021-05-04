# django

- Утсановка 
Предварительно необходимо установить нужные пакеты и зависимости:

```ruby
sudo yum -y install python3-dev python3-pip python3-virtualenv sqlitebrowser
```
Далее необходимо скопировать необходимые конфигурационные файлы и выполнить следующую команду
```ruby
pip3 install -r requirements.txt
```
После чего:
```ruby
[root@web2 django-main]# python3 manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying admin.0003_logentry_add_action_flag_choices... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying auth.0010_alter_group_name_max_length... OK
  Applying auth.0011_update_proxy_permissions... OK
  Applying sessions.0001_initial... OK
  ```
  Для доступа к админскому интерфейсу создадим юзера и пароль:
 ```ruby
[root@web2 django-main]# python3 manage.py createsuperuser --username admin --email admin@test.com
Password:
Password (again):
Superuser created successfully.
```
Теперь можем запускать сервер
```ruby
[root@web2 django-main]# python3 manage.py runserver
```
![image](https://user-images.githubusercontent.com/69155591/117031735-b14c6800-ad22-11eb-8d59-49f12e158c6f.png)
![image](https://user-images.githubusercontent.com/69155591/117031833-c75a2880-ad22-11eb-8dce-d2a9c6f26466.png)


