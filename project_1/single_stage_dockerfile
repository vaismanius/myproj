# Copies in our code and runs NPM Install
# Phase I
FROM python:3.6 as builder
WORKDIR /usr/src/app
COPY flask-api/ ./
RUN pip install -r requirements.txt
# fixed the requirements to also have pylint in it
# Running Unit TESTS
RUN ["make", "test"] #
RUN ["pylint", "--rcfile=pylint.cfg", "run_app.py"]
CMD ["python", "run_app.py"]
