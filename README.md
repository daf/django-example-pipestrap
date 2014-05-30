django-example-pipestrap
========================

Sample repository for django-pipeline / django-twitter-bootstrap issue (estebistec/django-twitter-bootstrap#15)

To reproduce (assumes virtualenv):

```
git clone git@github.com:daf/django-example-pipestrap.git
cd django-example-pipestrap

mkvirtualenv --no-site-packages django-example-pipestrap
workon django-example-pipestrap
pip install -r requirements.txt

python manage.py syncdb
python manage.py runserver 8888
```

Then visit `localhost:8888` in your browser.  You should get an error when it tries to import a bootstrap LESS file:

```
CompilerError at /
[31mFileError: 'twitter_bootstrap/less/variables.less' wasn't found[39m[31m in [39m/Users/dfoster/Documents/Dev/code/django-example-pipestrap/basic/static/newt.less[90m on line 1, column 1:[39m
1 [7m[31m[1m@[22mimport "twitter_bootstrap/less/variables.less";[39m[27m
[90m2 [39m[0m[0m
```



