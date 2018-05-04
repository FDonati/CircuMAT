**RaMa-Scene web-application**
---
RaMa-Scene is a django 2.0 based web-application that allows for analyzing Environmentally Extended Input-Output (EEIO) tables. EXIOBASE v3.3 is used in this project. 

**Documentation**
---
TODO

**Getting started**
---
Clone the data repository: git clone https://SidneyNiccolson@bitbucket.org/CML-IE/rama-scene_data.git

Clone the project: git clone https://SidneyNiccolson@bitbucket.org/CML-IE/rama-scene.git

Point in settings.py to the data repository files: PATH_TO_L, PATH_TO_B, PATH_TO_Y

Create a virtual environment and install the app requirements : $pip3 install -r requirements.txt

Install node.js:     $sudo apt-get update
    		     $sudo apt-get install nodejs

On debian install nodejslegacy: $sudo apt-get install nodejs-legacy

Install redis: $sudo apt install redis-server

[Perform next steps while in virtualenv and in the rootfolder of the project]

Prepare the database by running: $python3 manage.py makemigrations and $python3 manage.py migrate

Populate the database by running: $python3 manage.py populateHierarchies

Prepare static resources (node version: 3.10.10 or higher): $npm install

Built React bundle: $./node_modules/.bin/webpack --config webpack.config.js

Start Celery: $celery -A ramasceneMasterProject worker -l info  --concurrency=2 

Start the development server: $python3 manage.py runserver

**Core dependencies**
---
The app uses Celery [4.1.0] (http://docs.celeryproject.org/en/latest/django/first-steps-with-django.html), Django channels [2.0.2] (https://channels.readthedocs.io/en/latest/) and React [16.2.0] (https://reactjs.org/)
