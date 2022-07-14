FROM python:3.8
LABEL maintainer="Khaled Saleh"
COPY . ./app
WORKDIR /app

RUN python -m pip install --upgrade pip
##
#RUN pip freeze > requirements.txt 

COPY requirements.txt /tmp/
RUN pip install --requirement /tmp/requirements.txt
#RUN pip install -r requirements.txt

ENV PORT=3111
EXPOSE $PORT


##
#RUN pip freeze > init_db.py
COPY init_db.py /tmp/
RUN python3 /tmp/init_db.py
#RUN python3 ./init_db.py
CMD ["python", "app.py"]
