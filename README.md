
# Transfer Data From Sqlite To Other Databases In Django
<br>
Whenever a person starts learning Django, she/he starts from Sqlite database. And by the time you know most of the Django, you realize that that your most important data is in the Sqlite and now you would want to use high end databases like PostgreSQL or MySQL. 
<br>
<br>
In order to achieve that, do the following steps in order :
<br>
<br>

```shell

python manage.py dumpdata > db.json

```

Change the database settings to new database such as of MySQL / PostgreSQL.

```shell

python manage.py migrate

```

```shell

python manage.py shell

```

Enter the following in the shell

```shell
from django.contrib.contenttypes.models import ContentType
ContentType.objects.all().delete()
```

```shell
python manage.py loaddata db.json
```
