web: gunicorn django_sample.wsgi --limit-request-line 8188 --log-file -
worker: celery worker --app=django_sample --loglevel=info
