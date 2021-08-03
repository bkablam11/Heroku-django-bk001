"# Heroku-django-bk001"

Token : 0b01f9d120ef265975712b2855062ecf40200570

Use this token for our API by setting a request header called Authorization, followed by Token <token>, eg:
	
import requests
username = 'bkablam10'
token = '0b01f9d120ef265975712b2855062ecf40200570'

response = requests.get(
    'https://www.pythonanywhere.com/api/v0/user/{username}/cpu/'.format(
        username=username
    ),
    headers={'Authorization': 'Token {token}'.format(token=token)}
)
if response.status_code == 200:
    print('CPU quota info:')
    print(response.content)
else:
    print('Got unexpected status code {}: {!r}'.format(response.status_code, response.content)) 


# git

$ git init
Initialized empty Git repository in ~/djangogirls/.git/
$ git config --global user.name "Your Name"
$ git config --global user.email you@example.com 
$ git status
$ git add .
$ git commit -m "My Django Girls app, first commit"
$ git branch -M main
$ git remote add origin https://github.com/<your-github-username>/my-first-blog.git
$ git push -u origin main (master)
....
# pythonAnyWhere
Configurer votre site sur PythonAnywhere
Allez sur le Panneau de Contrôle de PythonAnywhere en cliquant sur le logo, et choisissez l'option de démarrer un terminal "Bash". C'est comme votre terminal à vous, mais chez PythonAnywhere.
..
$ pip3.8 install --user pythonanywhere
$ pa_autoconfigure_django.py --python=3.8 https://github.com/<your-github-username>/my-first-blog.git (or pa_autoconfigure_django.py --python=3.8 https://github.com/bkablam11/Heroku-django-bk001.git --nuke
)
(ola.pythonanywhere.com) $ python manage.py createsuperuser
(ola.pythonanywhere.com) $ ls
(ola.pythonanywhere.com) $ ls blog/
## link
https://tutorial.djangogirls.org/fr/django_urls/


## Commiter et pusher votre code sur GitHub a nouveau
$ git status
$ git add .
$ git status
$ git commit -m "Modification du HTML du site"
$ git push

## Puller les modifications sur PythonAnywhere et recharger son appli web
$ cd ~/<your-pythonanywhere-domain>.pythonanywhere.com
$ git pull
