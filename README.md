# django-docker-base
command

    docker-compose run --rm web django-admin startproject djangoproject .
    
settings.py
    
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql_psycopg2',
            'NAME': 'postgres',
            'USER': 'postgres',
            'PASSWORD': 'password',
            'HOST': 'db',
            'PORT': 5432,
        }
    }

    LANGUAGE_CODE = 'ja'
    
    TIME_ZONE = 'Asia/Tokyo'

command

    docker-compose run --rm web python manage.py migrate
    docker-compose run --rm web python manage.py createsuperuser