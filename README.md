# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
file:///home/sec/Downloads/entity.png![image](https://user-images.githubusercontent.com/118657189/208285177-86bdfa8a-105c-4402-8610-14569588e0dd.png)


## DESIGN STEPS

### STEP 1:
Create a new Django project using "django-admin startproject", get into the project terminal and use "python3 manage.py startapp"command.

### STEP 2:
Define a model for the students_marks in the models.py. Allow host access and add the app name under installed apps in settings.py

### STEP 3:
Register the models with the Django admin site. In admin.py under app folder, register the models with Django admin site.

### STEP 4:
Run the python manage.py makemigrations and python manage.py migrate commands to create the necessary database tables for the student_marks model. Run the server using "python3 manage.py runserver 0:80" command.


## PROGRAM
#IN models.py:-
```
from django.db import models
from django.contrib import admin
#Create your model here.
class student_marks(models.Model):
    register_no = models.IntegerField(primary_key=True)
    physics =models.FloatField()
    chemistry = models.FloatField()
    computer = models.FloatField()
    maths = models.FloatField()
    english= models.FloatField()
    total= models.FloatField()
class student_marksAdmin(admin.ModelAdmin):
    list_display = ('register_no','physics','chemistry','computer','maths','english','total')
```

#IN admin.py:-
```
from django.contrib import admin
from .models import student_marks,student_marksAdmin

admin.site.register(student_marks,student_marksAdmin)
```

## OUTPUT
file:///home/sec/Downloads/output.png![image](https://user-images.githubusercontent.com/118657189/208285226-94fd26c6-f9c7-4c10-b9b4-32e53bfeff4f.png)


## RESULT
Successfully developed a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
