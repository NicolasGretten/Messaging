#
FROM python:3.9

#
RUN mkdir -p /code
WORKDIR /code

#
COPY ./requirements.txt /code/requirements.txt

#
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

#
COPY ./app /code/app

#
CMD [ "python", "./app/main.py"]

