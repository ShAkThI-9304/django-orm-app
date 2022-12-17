# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
Column name | Column Type
------------ | -------------
Name | CharField
pin | IntegerField
bank_account_num | IntegerField
contact_num | IntegerField
email | EmailField

## DESIGN STEPS

### STEP 1:
An Django application is created inside dataproject folder.

### STEP 2:
A python program is written to create a table to store and retrieve data.

### STEP 3:
The table is created with 6 fields in which the username field is made as PrimaryKey.

### STEP 4:
Then the project files migrated. A superuser is also created.

### STEP 5:
Now the server side program is executed .

### STEP 6:
The admin page of our website is accessed using username and password.

### STEP 7:
Records are added and saved in the table inside the database.



## PROGRAM

```
from django.db import models
from django.contrib import admin

class bankdata(models.Model):
    name_primary_key = models.CharField(max_length=30)
    pin = models.CharField(max_length=30)
    bank_account_num = models.IntegerField(primary_key=True,unique=True)
    contact_num = models.IntegerField()
    email = models.EmailField(max_length=50,unique=True)

class bankadmin(admin.ModelAdmin):
    list_display = ('name_primary_key', 'pin', 'bank_account_num', 'contact_num','email')

```

## OUTPUT

![Django-data-base](django-data.png)


## RESULT
Thus a Django application is successfully developed to store and retrieve data from a database using Object Relational Mapping(ORM).