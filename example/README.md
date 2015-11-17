Set the environment variables 

    source source 'path_to'/sa_config.sh 

Generate the required database

    dbinit -z "UTF8BIN" -zn "UCA" -i -dba "dba","***" -t "django.log" "/Users/peterrosemann/Desktop/django.db"

Start the database server

    nohup dbsrv17 django.db

Generate the django db tables

    python manage.py migrate


Generate the django local admin user


   python manage.py createsuperuser

Run the django instance against the db server

   python manage.py runserver 0:8000

Use the browser and access the django admin framework

   http://localhost:8000/admin

Enjoy!
