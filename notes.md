# 
This is from a Django Crash Course which can be found [here](https://www.youtube.com/watch?v=0roB7wZMLqI&ab_channel=freeCodeCamp.org).

## Create Env, Install Django, Run Env
```sh
pip install pipenv
pipenv install django
pipenv shell
```

## Create Project and Application
```sh
django-admin startproject <project_name>
cd <project_name>
python manage.py startapp <app_name>
```

## Run Application
```sh
python manage.py runserver
```

## Migration
From `<root_dir>/<project_name>`:
```sh
python manage.py makemigrations

python manage.py migrate
```

## Creating sqlite3 Users
To create a superuser:
```sh
python manage.py createsuperuser
```
After creating, users can be added via 127.0.0.1:8000/admin/auth/user/add when server is running.

## mysql database
I've added a mysql server in `docker-compose.yml` to run locally.
### Connect to DB
```sh
mysql -h 127.0.0.1 -P 3306 -u root -p
```
### Installing client
```sh
pipenv install mysqlclient
```