FROM python:{{cookiecutter.python_version}}-slim-buster

RUN pip install poetry

ADD poetry.lock pyproject.toml /opt/app/
WORKDIR /opt/app

RUN poetry config virtualenvs.create false \
  && poetry install --no-dev --no-interaction --no-ansi

ADD . /opt/app
