# Item catalog project
udacity Full Stack Web Developer Nanodegree Project 3 - Item Catalog

##Files
* application.py -- python script with flask main application
* catalog.db -- sqlite database for item catalog
* database_setup.py -- pathon script for sqlalchemy database schema
* addData.py -- python script to polulate database with sample data
* static/styles.css -- css style for all views
* templates/additem.html -- template for item add view
* templates/catalog.html -- template for catalog and category overview
* templates/deleteitem.html -- template for item delete view
* templates/edititem.html -- template for item edit view
* templates/item.html -- template for item view
* templates/header.html -- header for all views
* templates/footer.html -- footer for all views

## Requirements

* python
* [flask](http://flask.pocoo.org) 
* [sqlalchemy](http://www.sqlalchemy.org)
* [SeaSurf](https://flask-seasurf.readthedocs.org)
* [GitHub-Flask](https://github-flask.readthedocs.org/en/latest/)

##Setup
for GitHub OAuth the Client ID and Client Secret have to be changed in application.py: 

```python
app.config['GITHUB_CLIENT_ID'] = 'XXX'
app.config['GITHUB_CLIENT_SECRET'] = 'YYY'
```

for session managment you should change the secret key of the app:
```python
app_secret = 'ZZZ'
```

the callback url should be something like https://dev.danielburkard.de/github-callback and can be configured in the head of application.py:
```python
github_callback_url = "https://dev.danielburkard.de/github-callback"
```

reset database:
```bash
[vagrant@vagrant:catalog] rm catalog.db
[vagrnt@vagrant:catalog] python addData.py
```

##Usage
start application
```bash
[vagrant@vagrant:catalog] python application.py
```

##Example
https://dev.danielburkard.de (login needed)
