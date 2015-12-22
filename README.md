$ heroku --version
heroku-toolbelt/3.42.25 (x86_64-linux) ruby/1.9.3
heroku-cli/4.27.9-cce0260 (amd64-linux) go1.5.2

If you don't have heroku installed please go to
https://toolbelt.heroku.com/

$ heroku login
Enter your Heroku credentials.
Email: youremail@example.com
Password:
Uploading ssh public key /Users/joe/.ssh/id_rsa.pub

$ virtualenv ENV
New python executable in ENV/bin/python
Installing setuptools, pip...done.

$ source ENV/bin/activate

(ENV)$ git clone git@github.com:yangxu/heroku-django-empty-template.git
Cloning into 'heroku-django-empty-template'...
Warning: Permanently added the RSA host key for IP address 'x.x.x.x' to the list of known hosts.
remote: Counting objects: 12, done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 12 (delta 0), reused 12 (delta 0), pack-reused 0
Receiving objects: 100% (12/12), done.
Checking connectivity... done.

(ENV)$ cd heroku-django-empty-template
(ENV)$ pip install -r requirements.txt

