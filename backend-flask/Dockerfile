FROM python:3.10-slim-buster

WORKDIR /backend-flask

#Contains libraries we want to install to run the app
COPY requirements.txt requirements.txt
#Instal; the python librariess used for the app
RUN pip3 install -r requirements.txt

# first . means everything in the current directory so everything in /backend-flask outside the container and second . represents /backend-flask inside container
COPY . .

#Sets environment variables inside the container and will remain set when the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD = command 
#The command used to run flask
#Specifying flask module, binding to --host=0.0.0.0" (everything address) and start on this port --port=4567
#Run on CLI python3 -m flask run --host=0.0.0.0 --port=4567
#Append /api/activities/home to URL
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]