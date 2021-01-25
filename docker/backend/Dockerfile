###########################################################################################################
FROM python:3.9.1

# set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# add requirements (to leverage Docker cache)
ADD ./backend/requirements.txt /usr/src/app/requirements.txt

# install requirements
RUN pip install -r requirements.txt

# add app
ADD ./backend /usr/src/app

# run server
RUN python manage.py makemigrations
RUN python manage.py migrate
CMD python manage.py runserver 0.0.0.0:8000
###########################################################################################################
