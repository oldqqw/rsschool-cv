![](<img src="http://www.google.com.au/images/nav_logo7.png">)

### Anton Gerasimov
### Contacts:
[Telegram](https://t.me/gerasimovtltsu)
[Discord](https://discordapp.com/users/912402722853101578/)
### Brief information about yourself
I want to become a Javascript developer. I quickly learn new material. For a long time I developed a Django backend for myself. There is a desire to learn JS.
### Skills
Python, Django
### Code examples
```Python
from django.db import models

class Category(models.Model):
    """ Класс для категорий обращений """
    cat_name = models.CharField(max_length=64, verbose_name='Категория') # Имя категории

    class Meta:
        verbose_name = 'Категории'
        verbose_name_plural = 'Категории'
    
    def __str__(self):
        return self.cat_name

class FreeDateTime(models.Model):
    """ Класс для внесения свободного времени """
    free_times = models.CharField(max_length=64, verbose_name='Свободное время') # Свободное время
    reserved_status = models.BooleanField(default=False) # Проверка занятости

    class Meta:
        verbose_name = 'Свободное время'
        verbose_name_plural = 'Свободное время'

    def __str__(self):
        return '%s' % (self.free_times)

class Consult(models.Model):
    """ Класс для оформления записи """
    category = models.ForeignKey(Category, on_delete=models.CASCADE, max_length=120, verbose_name='Категория')
    date_time = models.CharField(max_length=20, verbose_name='Дата и время') # Время для записи
    fcs = models.CharField(max_length=120, verbose_name='ФИО') # ФИО
    phone = models.CharField(max_length=16, verbose_name='Телефон для связи') # Телефон для связи
    description = models.CharField(max_length=1000, verbose_name='Описание проблемы') # Описание проблемы

    class Meta:
        verbose_name = 'Активные записи'
        verbose_name_plural = 'Записи на консультацию'
    
    def __str__(self):
        return '%s' % (self.description)
```

### Work experience
Developed Django projects for myself

### Education
Bachelor in the specialty "Mathematical support and administration of information systems"

### English level
A2-B1