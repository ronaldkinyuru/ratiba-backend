#Ratiba_Events
Django install
how to run
sudo service postgresql start
source venv/bin/activate
python3 manage.py runserver

1. python3 -m pip install virtualenv.   -install package

2. python3 -m venv venv - create virtual env
3. source venv/bin/activate - activate for Ubuntu/Mac

pip install -r requirements.txt


4. python3 -m pip install Django
5. pip install --upgrade pip
6. python3 -m pip install djangorestframework


7. django-admin startproject <name_of_project>
8. python3 manage.py startapp <name_of_app>
9. Modify settings.py for project file under ‘installed_apps’ to include ‘rest_framework’ and <name_of_app>

#Documentation
https://drf-yasg.readthedocs.io/en/stable/readme.html#usage
https://swagger.io/resources/open-api/

#Databases
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo service postgresql start

psql -U postgres
CREATE DATABASE ratiba_db;
CREATE USER ratiba_user WITH PASSWORD 'your_password';
GRANT ALL PRIVILEGES ON DATABASE ratiba_db TO ratiba_user;

#Deletion
python manage.py shell
from authentication.models import User
User.objects.all().delete()

#Verification
python manage.py shell
from authentication.models import User
User.objects.get(email='').is_verified

#Flushing tokens
python manage.py flushexpiredtokens
