# DjangoBasicAuth  
## This is a very basic Django App making use of Django's builtin authentication and bootstrap-5

You can `start a project` and clone the accounts app very simply. Just Copy and paste the accounts directory in your project  

#### Also Install the req.txt mean while 
```
pip install req.txt
```


## Add following codes in settings.py 

```python
INSTALLED_APPS = [
    #....
    'accounts',
    'bootstrap5', # add these
]
```

### After that 

```python
# add these at very bottom of settings.py
LOGIN_REDIRECT_URL = '/'
LOGOUT_REDIRECT_URL = '/'
```

### Make sure `APP_DIRS` is set to `True`

```python

TEMPLATES = [
    {
        #...
        'APP_DIRS': True,
        #...
        },
    },
]

```

## We also need to modify the urls.py in the root directory     

```python
# add include
from django.urls import path,include

urlpatterns = [
    #add the accounts in the urls
    path('accounts/', include('accounts.urls'))
]
```
