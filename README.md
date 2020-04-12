# Django Boilerplate

This is a boilerplate I created for starting Django projects.

Repo can be cloned and renamed with "python manage.py rename YourChosenName"


NOTE: You must create a .env to the root folder of this project. This file will contain the following:

SECRET_KEY=yoursecretkey
DEBUG=True
DB-NAME=your-db-name
DB-USER=your-db-user-name
DB-PASSWORD=your-db-password
DB-HOST=your-db-host
STRIPE_PUBLIC_KEY = 'your-live-public-key'
STRIPE_SECRET_KEY = 'your-live-secret-key'

The SECRET_KEY is a 32 character long string that is usually located in settings.py, but since this project has base.py and a .env file, this key is not visible anywhere.

You can create the SECRET_KEY by running the following:

python manage.py shell

>>> from django.core.management.utils import get_random_secret_key
>>> get_random_secret_key()
'[GENERATED KEY]'
>>>

Note: The >>> represents the shell prompt, and should not be typed.

Once you have the SECRET_KEY, copy paste it to the .env file and run python manage.py migrate to apply the correct migrations.

After this you should be good to go and continue with your project