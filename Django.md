## Django - Cheat Sheet

Set up a new virtual environment named env.
```shell
python3 -m venv env
```

Activate the virtual environment.
```shell
source env/bin/activate
```

Install Django into the dedicated dev workspace. (This command it's used to install packages in the dev environment).
```shell
python3 -m pip install django
```

Pin the dependencies to make sure that we are keeping track of which Django version we have installed.
```shell
python3 -m pip freeze > requirements.txt
```

You should always include a record of the versions of all packages you used in your project code, such as in a requirements.txt file. The requirements.txt file allows you and other programmers to reproduce the exact conditions of your project build.

Suppose you’re working on an existing project with its dependencies already pinned in a requirements.txt file.
In that case, you can install the right Django version as well as all the other necessary packages in a single command.
```shell
python3 -m pip install -r requirements.txt
```

Create a Django project.
```shell
django-admin startproject <name-of-project>
```

Start a new app
```shell
python manage.py startapp <name-of-project>
```

Verify if Django is installed.
```python
import django
django.get_version()
```

Files important.

> __init__: Define their containing folders as packages.
> migrations/: Will hold information about changes to yout future database.
> models.py; Will define the data model for your app.
> views.py: Will handle the logic controlling the app display.