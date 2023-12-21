FROM python:3.7

RUN apt update -y

COPY requirements.txt /tmp/requirements.txt

RUN --mount=type=cache,target=/root/.cache/pip \
    pip install -U pip && \
    pip install -r /tmp/requirements.txt

WORKDIR /code/

COPY . /code/

WORKDIR /code/app

CMD python app.py
