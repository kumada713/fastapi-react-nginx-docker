FROM python:3.8

WORKDIR /usr/src/app

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip && \
    pip install pipenv

COPY ./backend/Pipfile ./backend/Pipfile.lock /usr/src/app/

RUN pipenv install --system --ignore-pipfile --deploy

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8080"]