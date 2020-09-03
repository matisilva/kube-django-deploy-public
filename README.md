# Despliegue de sistemas predictivos - Práctico 1
> Diplodatos 2019

En este proyecto, construiremos y desplegaremos nuestra propia API que brindará servicios de Machine Learning, en este caso, predicción de sentimientos para oraciones en Español.

La estructura base del proyecto será la siguiente:

```
├───apps
│   └───brounder
│       │   .dockerignore
│       │   .gitignore
│       │   docker-compose.yml
│       │   Dockerfile
│       │   manage.py
│       │   README.md
│       │   requirements.txt
│       │   __init__.py
│       │
│       ├───brounder
│       │       settings.py
│       │       urls.py
│       │       wsgi.py
│       │       __init__.py
│       │
│       └───guestbook
│           │   admin.py
│           │   apps.py
│           │   models.py
│           │   tests.py
│           │   urls.py
│           │   views.py
│           │   __init__.py
│           │
│           ├───migrations
│           │       0001_initial.py
│           │       0001_initial.pyc
│           │       __init__.py
│           │       __init__.pyc
│           │
│           ├───static
│           │   └───js
│           │           controllers.js
│           │
│           └───templates
│                   index.html
│
└───kubernetes
    ├───brounder
    │       brounder.yml
    │
    ├───postgres
    │       postgres.yml
    │
    └───redis
            redis.yml
```

Veamos una descripción rasgos generales de cada modulo:

Su tarea será completar con el código correspondiente cada .yml de la carpeta kubernetes y el docker-compose.yml de la carpeta apps
