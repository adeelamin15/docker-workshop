# our base image
FROM python:3.8-slim-buster

WORKDIR /usr/src/app/

# install Python modules needed by the Python app
COPY requirements.txt .
RUN python -m pip install -r requirements.txt

# copy files required for the app to run
COPY app.py .
COPY templates/index.html ./templates/

# tell the port number the container should expose
EXPOSE 5000

# run the application
CMD ["python", "app.py"]

