# Ex02 Django ORM Web Application
# Date:17/10/26
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 cars

# PROGRAM

admins.py
```
from django.contrib import admin
from .models import Student

class StudentAdmin(admin.ModelAdmin):
    list_display = ('IDNo', 'name', 'age', 'DOB', 'phone_number', 'mother_name', 'father_name')
admin.site.register(Student, StudentAdmin)
```

models.py
```
from django.db import models
class Student(models.Model):
    IDNo = models.BigAutoField(primary_key=True)
    name = models.CharField(max_length=20)
    age = models.IntegerField(blank=True)
    DOB=models.DateField(blank=True)
    phone_number=models.IntegerField(null=True,default=0)
    mother_name=models.CharField(max_length=30,default='NA')
    father_name=models.CharField(max_length=30,default='NA')
```

urls.py
```
from django.contrib import admin
from django.urls import path
from app import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.home)
]
```
# OUTPUT
![alt text](<Screenshot 2026-10-10 131411.png>)



# RESULT
Thus the program for creating a database using ORM hass been executed successfully
