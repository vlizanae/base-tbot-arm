FROM arm64v8/python:alpine

USER root
WORKDIR /root

RUN apk add --no-cache --virtual .build-deps build-base libffi-dev openssl-dev

RUN pip install python-telegram-bot requests
RUN adduser telegram -h /home/telegram -D

RUN apk del .build-deps

COPY Santiago /etc/localtime

USER telegram
WORKDIR /home/telegram

