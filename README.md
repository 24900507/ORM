# EX 02 Django ORM Web Application
## Developed by : AKASH G
## Register No. : 212224100004
## Date: 28.08.2025

## AIM
To develop a Django application to store and retrieve data from Car Inventory Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

<img width="1090" height="588" alt="image" src="https://github.com/user-attachments/assets/14916276-80e9-450b-a49f-14bc77d149ba" />


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM : 
```
admin.py
from django.contrib import admin
from .models import Car

@admin.register(Car)
class CarAdmin(admin.ModelAdmin):
    list_display = ('car_id', 'brand', 'model', 'year', 'price')
    search_fields = ('brand', 'model')
    list_filter = ('year', 'brand')


model.py
from django.db import models

class Car(models.Model):
    car_id = models.AutoField(primary_key=True)
    brand = models.CharField(max_length=100)
    model = models.CharField(max_length=100)
    year = models.IntegerField()
    price = models.FloatField()

    def _str_(self):
        return f"{self.brand} {self.model} ({self.year})"

```

## OUTPUT

<img width="1440" height="900" alt="Screenshot 2025-11-26 at 11 46 51 PM" src="https://github.com/user-attachments/assets/67804671-6130-4e1d-96c9-6af6926bc90e" />
<img width="1440" height="900" alt="Screenshot 2025-11-26 at 11 54 56 PM" src="https://github.com/user-attachments/assets/da490f2f-fb40-4c2c-80c5-5b250ebcab9b" />


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
