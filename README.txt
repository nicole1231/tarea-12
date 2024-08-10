The app will not work without a database, so you should make a local_settings.py in the same folder as the settings.py, i use postgre so this config is for postgre only  
The local_settings.py needs to be like this:                  

DATABASES = {
    'default': {
        'ENGINE': "django.db.backends.postgresql",
        'NAME': 'db name',
        'USER': 'db_user (postgres is a default user for any db, you can use it if you want)',
        'PASSWORD': 'Here is the user password, if you are not sure wich password your user has you can execute ALTER USER your_user WITH PASSWORD 'new_password'; while you are in the db',
        'HOST': '127.0.0.1 (this is the local host)',
        'PORT': '5432 (this is the local host port, if it does not work you can use 8000 (im not sure if it is a solid solution tho))',
    }
}  

