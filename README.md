# Django 4.1 Tutorial (until part 5)
This project is based on the [Django documentation 4.1 Tutorial](https://docs.djangoproject.com/en/4.1/intro/tutorial01/) (until part 5).

## Installing

To install and execution the API in your local machine, you will need to:

```
a)
git clone https://github.com/RicardoTurco/django_tutorial_41_until_part5 && cd django_tutorial_41_until_part5

b)
Create and activate one "virtualenv"
(using any valid form) 

c)
This next 2 steps are OPTIONAL, but HIGH recommended !!!
1) python -m pip install --upgrade pip
2) pip install -U setuptools

d)
pip install -r requirements.txt

e)
Run MAKEMIGRATIONS and MIGRATE comands to create a BD (sqlite):
1) python manage.py makemigrations
2) python manage.py migrate

f)
Create a "superuser" to access django-admin:
python manage.py createsuperuser

g)
Run the appliation:
python manage.py runserver
```
