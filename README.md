# Django Sample
Made with https://github.com/vintasoftware/django-react-boilerplate

## Setup
- On project root, do the following:
- Create a copy of ``django_sample/settings/local.py.example``:  
  `cp django_sample/settings/local.py.example django_sample/settings/local.py`
- Create a copy of ``.env.example``:  
  `cp .env.example .env`
- Create the migrations for `users` app (do this, then remove this line from the README):  
  `python manage.py makemigrations`
- Run the migrations:  
  `python manage.py migrate`

## Tools
- Setup [editorconfig](http://editorconfig.org/), [prospector](https://prospector.landscape.io/en/master/) and [ESLint](http://eslint.org/) in the text editor you will use to develop.

## Running the project
- `pip install -r requirements.txt`
- `npm install`
- `npm run start`
- `python manage.py runserver`

## Testing
`make test`

Will run django tests using `--keepdb` and `--parallel`. You may pass a path to the desired test module in the make command. E.g.: `make test someapp.tests.test_views`

## Adding new pypi libs
Add high level dependecies to `requirements-to-freeze.txt` and `pip freeze > requirements.txt`. This is [A Better Pip Workflow](http://www.kennethreitz.org/essays/a-better-pip-workflow).

## Linting
- Manually with `prospector` and `npm run lint` on project root.
- During development with an editor compatible with prospector and ESLint.

## Pre-commit hooks
- Run `pre-commit install` to enable the hook into your git repo. The hook will run automatically for each commit.
- Run `git commit -m "Your message" -n` to skip the hook if you need.

## Deploying
- `git clone` this repo in production (or `scp` files to it)
- Run `npm run build` to build static files with webpack
- Look inside `settings/production.py` for all `config` calls to find the necessary environment variables. Add them to a `.env` file in production only.
- Run with the project some wsgi server

Copyright (c) 2017 Vinta Serviços e Soluções Tecnológicas Ltda.
[MIT License](LICENSE.txt)
