FROM python:3.11.4-alpine

WORKDIR /usr/src/app

# Prevents Python from writing pyc files to disc
ENV PYTHONDONTWRITEBYTECODE 1

# ensure that the python output is sent straight to terminal without buffering it first
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip

COPY ./requirements.txt /usr/src/app/requirements.txt
RUN pip install -r requirements.txt

COPY ./entrypoint.sh /usr/src/app/entrypoint.sh

COPY . /usr/src/app/

ENTRYPOINT ["/usr/src/app/entrypoint.sh"]