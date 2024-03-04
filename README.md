# Ex02 Django ORM Web Application
## Date:  04.03.2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![alt text](image-2.png)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```
models.py
from django.db import models
from django.contrib import admin
class Book_DB(models.Model):
	slno=models.IntegerField(primary_key="slno");  
	bname=models.CharField(max_length=50);
	author=models.CharField(max_length=20);
	published_date=models.DateField();
	prize=models.IntegerField();
class BookAdmin(admin.ModelAdmin):
	list_display=("slno", "bname", "author", "published_date", "prize");

admin.py
from django.contrib import admin
from .models import Book_DB,Book_DBAdmin
admin.site.register(Book_DB,Book_DBAdmin)
```
## OUTPUT
![alt text](<Exp 2 WEB.png>)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully.