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
Follow the all instructions in the WORKFLOW item, to
add 'polls' and 'choices' in BD

h)
Run the tests to make sure the integrity of application:
python manage.py test polls

i)
Run the appliation:
python manage.py runserver

j)
Access in your browser 'localhost:8000/polls/' or '127.0.0.1:8000/polls/'
```

## WorkFlow:

Before to use the application, is necessary create some records in DB:

```
a) Acessing the interactive shell of python:

python manage.py shell


b) Create some Questions:

>>> from polls.models import Question

>>> from django.utils import timezone
>>> q = Question(question_text="What's up?", pub_date=timezone.now())
>>> q.save()

>>> Question.objects.all()
<QuerySet [<Question: What's up?>]>


c) Create some Choices:

>>> from polls.models import Choice

# Get de Question created ...
>>> q = Question.objects.get(pk=1)

# Create Choice 1:
>>> q.choice_set.create(choice_text='Not much', votes=0)
<Choice: Not much>

# Create Choice 2:
>>> q.choice_set.create(choice_text='The sky', votes=0)
<Choice: The sky>

>>> exit()
```
