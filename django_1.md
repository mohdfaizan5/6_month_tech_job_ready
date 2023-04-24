# Django <img href="google.com" src="https://user-images.githubusercontent.com/79694828/234032410-ad220037-688b-493c-886e-76d81f993937.png" width="35" height="35" />


    A web framework for python giving advangate to use wide variety of access to python


## Initial setup:

Creating a Virtual environment:
> Why virtual environment ?
>   When 


* manage.py --> a shortcut to use the django-admin command-line utility. It’s used to run management commands related to our project. We will use it to run the development server, run tests, create migrations and much more.
* __init__.py --> this empty file tells Python that this folder is a Python package.
* settings.py --> this file contains all the project’s configuration. We will refer to this file all the time!
* urls.py --> this file is responsible for mapping the routes and paths in our project. For example, if you want to show something in the URL /about/, you have to map it here first.
* wsgi.py --> this file is a simple gateway interface used for deployment. You don’t have to bother about it. Just let it be for now.


## Apps

* app: is a Web application that does something. An app usually is composed of a set of models (database tables), views, templates, tests.
* project: is a collection of configurations and apps. One project can be composed of multiple apps, or a single app.

### contains
```
python manage.py startapp home
```
* migrations/: here Django store some files to keep track of the changes you create in the models.py file, so to keep the database and the models.py synchronized.
* admin.py: this is a configuration file for a built-in Django app called Django Admin.
* apps.py: this is a configuration file of the app itself.
* models.py: here is where we define the entities of our Web application. The models are translated automatically by Django into database tables.
* tests.py: this file is used to write unit tests for the app.
* views.py: this is the file where we handle the request/response cycle of our Web application.

> Views are Python functions that receive an HttpRequest object and returns an HttpResponse object. Receive a request as a parameter and returns a response as a result.

* Reverse relationship in data base,

## Models
The models are basically a representation of your application’s database layout.

    
## related_name
The related_name parameter will be used to create a reverse relationship where the Board instances will have access a list of Topic instances that belong to it.

Django automatically creates this reverse relationship – the related_name is optional. But if we don’t set a name for it, Django will generate it with the name: (class_name)_set. For example, in the Board model, the Topic instances would be available under the topic_set property. Instead, we simply renamed it to topics, to make it feel more natural.

In the Post model, the updated_by field sets the related_name='+'. This instructs Django that we don’t need this reverse relationship, so it will ignore it.


> Django ORM, which is an abstraction layer that communicates with the database.





## Models API
```terminal
python manage.py shell
```
create, save, update

```
from <app_name>.models import <Model>
m1 = <Model>(property1= "", property2="..")
```
```
m1.save()
```
```
m1 # view it
m1.id # gives id of it
m1.property #gives value of the property
```

Every Django model comes with a special attribute; we call it a Model Manager. You can access it via the Python attribute objects. It is used mainly to execute queries in the database. For example, we could use it to directly create a new Board object:

```
board = Board.objects.create(name='Python', description='General discussion about Python.')
```

to get all objects from db
```
Board.objects.all()
```

Treat this queryset as list
```
boards_list = Board.objects.all()
for board in boards_list:
    print(board.description)
```

to get based on id or specific_value
```
django_board = Board.objects.get(id=1)
Board.objects.get(name='Django')
```


Operation	| Code sample
|---|---|
Create an object without saving	|board = Board()
Save an object (create or update)	|board.save()
Create and save an object in the database	|Board.objects.create(name='...', description='...')
List all objects	|Board.objects.all()
Get a single object, identified by a field|	Board.objects.get(id=1)


## Django Template Engine.




&bspm;
---
vocabulary

* skim 
* radial, meaning they start at the center and grow outward.
* important bits
* may be associated with 
* 

made some changes
....
...
...
