MAKEFLAGS+="-j 2"

FLASK_DEV=FLASK_APP="{{ cookiecutter.python_directory }}.{{ cookiecutter.app_file }}:create_app('dev')" FLASK_ENV=development

init:
	pip install -r requirements.txt
	cd "static/{{ cookiecutter.svelte_directory }}" && npm install

dev-python:
	$(FLASK_DEV) flask run

dev-vue:
	@npm run --prefix "static/{{ cookiecutter.svelte_directory }}" build:dev

dev: dev-python dev-vue
