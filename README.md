# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![django orm 0ut 1](https://user-images.githubusercontent.com/121412904/234750483-ade34bc1-04f9-443d-aa56-facc89dcd0e3.png)


## DESIGN STEPS

### STEP 1:
Clone the problem from github.
### STEP 2:
Create a new app.
### STEP 3:
Enter the code for admin.py and models.py
### STEP 4:
Create django app and add student details.
## PROGRAM
```
models.py 

from django.db import models
from django.contrib import admin


class Student(models.Model):
    referencenumber=models.CharField(primary_key=true,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email')

admin.py

from django.contrib import admin
from myapp.models import Student,StudentAdmin
admin.site.register(Student,StudentAdmin)
```

## OUTPUT

![Screenshot 2023-04-27 084711](https://user-images.githubusercontent.com/121412904/234751039-9c63b4fb-83b6-47e7-818b-112ab4ad131d.png)




## RESULT
Program executed successfully.
