## Social Blog

This project contains the social blogging application which allows us to post and edit blogs and let us comment on the blog. Others can also view and post comment on the blog.


### What's included
* User Authentication
* User Roles
* User Profiles
* Blog Posts
* Followers
* User Comments
* API
* Email

### Project Structure:

```
├── config.py
├── manage.py
├── Readme.md: documentation file
├── requirements.txt: requirements needs to be install
├── requirements
│   ├── common.txt: requirements needs to be install
│   ├── dev.txt: requirements needs to be install at the time of developement
│   └── prod.txt: requirements needs to be install at the time of production
├── app
│   ├── static: contains design data to load
│   ├── temaplates: contains design data to load
│   ├── __init__.py
│   ├── migrations: database migrations
│   ├── models.py: database models for app
│   ├── tests.py: test cases for view
│   ├── urls.py: urls for app
│   ├── forms.py: These forms are called by views
│   └── views.py: These views are called by urls
└── static
```

##### Initialize a virtualenv
```
$ pip install virtualenv
$ virtualenv -p python3 env
$ source env/bin/activate
```

##### Install the dependencies

```
$ pip install -r requirements.txt
```

##### Add Environment Variables

```
MAIL_USERNAME=GmailUsername
MAIL_PASSWORD=GmailPassword
SECRET_KEY=SuperRandomStringToBeUsedForEncryption
```

Other Key value pairs:

* `FLASKY_ADMIN`: set to the default email for your first admin account (default is `flasky@demo.com`)
* `DEV_DATABASE_URL`: set to a dev postgresql database url (default is `data-dev.sqlite`)
* `TEST_DATABASE_URL`: set to a test postgresql database url (default is `data-test.sqlite`)
* `DATABASE_URL`: set to a production postgresql database url (default is `data.sqlite`)

##### Create the database

```
$ python manage.py deploy
```

##### Run Server

```
python manage.py runserver
```
