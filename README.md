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
