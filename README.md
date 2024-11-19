# Ex02 Django ORM Web Application
## Date: 19.11.24

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![image](https://github.com/user-attachments/assets/161ee610-bf66-4e29-875f-09fdf14eba67)


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
admin.py
```
from django.contrib import admin
from .models import Bankloan,BankloanAdmin
admin.site.register(Bankloan,BankloanAdmin)
```
models.py
```
from django.db import models
from django.contrib import admin
class Bankloan (models.Model):
    Loanid=models.IntegerField(primary_key=True);
    Name=models.CharField(max_length=100);
    Age=models.IntegerField(default=18);
    emailid=models.CharField(max_length=100);
    phone=models.IntegerField();
    City=models.CharField(max_length=20, default='Chennai');
    Accountno=models.IntegerField();
    Salary=models.IntegerField();
    Loanamt=models.IntegerField();

class BankloanAdmin(admin.ModelAdmin):
    list_display=('Loanid','Name','Age','emailid','phone','City','Accountno','Salary','Loanamt')
```
## OUTPUT

![image](https://github.com/user-attachments/assets/e3ea497c-2c0e-4657-9d96-1c079e52b2fc)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
