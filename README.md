# django-docker-base

1

    docker-compose build

2

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

3

    docker-compose run --rm web python manage.py makemigrations
    docker-compose run --rm web python manage.py migrate
    docker-compose run --rm web python manage.py createsuperuser