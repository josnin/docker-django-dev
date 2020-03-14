# docker-django-dev
Docker container to isolate django dev. environment


### Goto to your Django App workdir
```bash
[josnin@localhost docker-django-dev]$ ls -l
total 12
-rw-rw-r--. 1 josnin josnin   12 Mar 14 10:29 requirements
drwxrwxr-x. 3 josnin josnin 4096 Mar 14 10:33 testdjango 
```


### Run django dev server (Used --net=host to use host network)
```
[jose@localhost docker-django-dev]$ docker run -it --net=host --rm -w /app/testdjango josnin/django-dev:v1
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 17 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.

March 14, 2020 - 03:19:31
Django version 2.2, using settings 'testdjango.settings'
Starting development server at http://0.0.0.0:8000/
Quit the server with CONTROL-C.

```
