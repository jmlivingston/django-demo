# Django Demo

This project is a way to quickly setup a barebones Django environment.

## Requirements

- [Node >= 6.0](https://nodejs.org)
- [Python >= 3.0](https://www.python.org)
- [Yarn](https://yarnpkg.com) (optional - you can replace yarn commands with npm)

## Start from Scratch

If you don't want to clone this project, you can start by running the following commands in your terminal.

> Note: I explicitly call my virtual environment "venv" to make it obvious. I also install Django in a server directory to keep the base directory clean, minimal, and descriptive. For example, we may add a "ui" or "client" directory for front-end resources.

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

Adding the following scripts to your package.json allows an easy way to install, migrate, and run your server.

```bash
"scripts": {
  "install": "yarn && python3 -m venv venv && . venv/bin/activate && pip install -r requirements.txt && exit",
  "migrate": ". venv/bin/activate && python server/manage.py migrate",
  "start": ". venv/bin/activate && python server/manage.py runserver"
}
```

Install after git clone

```bash
yarn run install
```

Migrate files to database (python)

```bash
yarn run migrate
```

Start server (python)

```bash
yarn run start
```