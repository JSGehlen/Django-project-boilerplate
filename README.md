# Django Boilerplate

This is a boilerplate I created for starting Django projects.

Repo can be cloned and renamed with ```python manage.py rename YourChosenName```

## Installation: 

1: Run ```pip3 install -r requirements.txt``` to install the requirements for this project
2: Create a folder called "static_in_env" in the src folder
3: Create a .env to the root folder of this project. This file will contain the following:

```
SECRET_KEY=yoursecretkey
DEBUG=True
DB-NAME=your-db-name
DB-USER=your-db-user-name
DB-PASSWORD=your-db-password
DB-HOST=your-db-host
STRIPE_PUBLIC_KEY = 'your-live-public-key'
STRIPE_SECRET_KEY = 'your-live-secret-key'
```

The SECRET_KEY is a 32 character long string that is usually located in ```settings.py```, but since this project has ```base.py``` and a ```.env``` file, this key is not visible anywhere.

4: Create the ```SECRET_KEY``` by running the following ``` python manage.py shell```
Then type the following commands:

```
from django.core.management.utils import get_random_secret_key
get_random_secret_key()
'[GENERATED KEY]'
```

Once you have the ```SECRET_KEY```, copy paste it to the ```.env``` file and run ```python manage.py migrate``` to apply the correct migrations.

After this you should be good to go and continue with your project
