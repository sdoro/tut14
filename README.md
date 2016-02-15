## [Django 1.4 tutorial](https://docs.djangoproject.com/en/1.4/intro/tutorial04/)

### 0.init git

    # make https://github.com/sdoro/tut14
    # make a new workspace tut1 cloned from git@github.com:sdoro/tut14.git
    # start writing into README.md file
    git add README.md
    
### 1. build a virtual environment with django 1.4.2

    virtualenv $HOME/.env
    source $HOME/.env/bin/activate
    git add requirements.txt
    pip install -r requirements.txt
    git commit -m "1. build a virtual environment with django 1.4.2"
    git push

### 2. Creating a project

    django-admin.py startproject mysite
    cd mysite/
    ./manage.py runserver $IP:$PORT
    # test browsing http://tut14-sdoro.c9users.io/
    git add . ../README.md
    git git commit -m "Creating a project."
    git push

### Database setup

    # edit mysite/settings.py
    git add mysite/settings.py
    ./manage.py syncdb
    # set email/password to ubuntu@c9.io
    git add db
    git commit -m "Database setup"
    git push

### Creating a models

    manage.py startapp polls
    git add polls
    # edit polls/models.py
    git commit -m "Creating a models"
    git push

### Activating models

    # edit mysite/settings.py
    ./manage.py sql polls
    ./manage.py suncdb
    git commit -m "Activating models"
    git push
