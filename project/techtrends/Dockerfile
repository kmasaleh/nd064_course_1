FROM python:3.8
LABEL maintainer="Khaled Saleh"
COPY . ./app
WORKDIR /app
RUN pip freeze > requirements.txt 
RUN pip install -r requirements.txt
ENV PORT=3111
EXPOSE $PORT
RUN python3 ./init_db.py
CMD ["python", "app.py"]
