# Django Demo

## Requirements

- node
- python
- anthing else?

## Starting from Scratch

Run the following steps

```bash
python3 -m venv venv
. venv/bin/activate
pip install django
mkdir server
django-admin startproject main server
pip freeze > requirements.txt
python server/manage.py runserver
```

## Helper Scripts for package.json

```bash
"scripts": {
  "install": "yarn && python3 -m venv venv && . venv/bin/activate && pip install -r requirements.txt && exit",
  "migrate": ". venv/bin/activate && python server/manage.py migrate",
  "start": ". venv/bin/activate && python server/manage.py runserver"
}
```

- install - used to install everything after git clone
- migrate - migrates files to database (python)
- start - starts server (python)