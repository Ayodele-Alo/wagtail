FROM python:3.8.1-slim-buster

EXPOSE 8000

ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

COPY requirements.txt /
RUN pip install -r /requirements.txt

WORKDIR /app

COPY . /app/

RUN python manage.py migrate

CMD python manage.py runserver 0.0.0.0:8000
