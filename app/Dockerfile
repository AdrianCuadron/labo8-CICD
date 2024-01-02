FROM python:3.11-alpine

RUN apk update

RUN mkdir -p /code
WORKDIR /code

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

RUN apk add --no-cache gcc musl-dev linux-headers

COPY requirements.txt /code

RUN pip install -r requirements.txt

COPY app.py /code

CMD flask run

