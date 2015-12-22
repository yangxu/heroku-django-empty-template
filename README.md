```
$ heroku --version
heroku-toolbelt/3.42.25 (x86_64-linux) ruby/1.9.3
heroku-cli/4.27.9-cce0260 (amd64-linux) go1.5.2
```

If you don't have heroku installed please go to
https://toolbelt.heroku.com/

```
$ heroku login
Enter your Heroku credentials.
Email: youremail@example.com
Password:
Uploading ssh public key /Users/youremail/.ssh/id_rsa.pub
```
```
$ virtualenv ENV
New python executable in ENV/bin/python
Installing setuptools, pip...done.
```
```
$ source ENV/bin/activate
```
```
(ENV)$ git clone git@github.com:yangxu/heroku-django-empty-template.git
Cloning into 'heroku-django-empty-template'...
Warning: Permanently added the RSA host key for IP address 'x.x.x.x' to the list of known hosts.
remote: Counting objects: 12, done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 12 (delta 0), reused 12 (delta 0), pack-reused 0
Receiving objects: 100% (12/12), done.
Checking connectivity... done.
```
```
(ENV)$ cd heroku-django-empty-template
```
```
(ENV)$ pip install -r requirements.txt
```
```
(ENV)$ heroku create <app-name>
Creating simple-spring-9999... done, stack is cedar-14
http://simple-spring-9999.herokuapp.com/ | git@heroku.com:simple-spring-9999.git
Git remote heroku added
```
```
(ENV)$ git push heroku master
Counting objects: 11, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (9/9), done.
Writing objects: 100% (11/11), 4.01 KiB, done.
Total 11 (delta 0), reused 0 (delta 0)
-----> Python app detected
-----> No runtime.txt provided; assuming python-2.7.6.
-----> Preparing Python runtime (python-2.7.6)
-----> Installing Distribute (0.6.36)
-----> Installing Pip (1.3.1)
-----> Installing dependencies using Pip (1.3.1)
       Downloading/unpacking Django==1.9 (from -r requirements.txt (line 1))
       ...
       Successfully installed Django psycopg2 gunicorn dj-database-url dj-static static
       Cleaning up...
-----> Collecting static files
       0 static files copied.

-----> Discovering process types
       Procfile declares types -> web

-----> Compiled slug size is 29.5MB
-----> Launching... done, v6
       http://simple-spring-9999.herokuapp.com deployed to Heroku

To git@heroku.com:simple-spring-9999.git
* [new branch]      master -> master
```

```
(ENV)$ heroku run python manage.py syncdb
Running python manage.py syncdb attached to terminal... up, run.1
Creating tables ...
Creating table auth_permission
Creating table auth_group_permissions
Creating table auth_group
Creating table auth_user_groups
Creating table auth_user_user_permissions
Creating table auth_user
Creating table django_content_type
Creating table django_session
Creating table django_site

You just installed Django's auth system, which means you don't have any superusers defined.
Would you like to create one now? (yes/no): yes
Username (leave blank to use 'u53976'): kenneth
Email address: kenneth@heroku.com
Password:
Password (again):
Superuser created successfully.
Installing custom SQL ...
Installing indexes ...
Installed 0 object(s) from 0 fixture(s)
```
