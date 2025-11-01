FROM python:3.12-bookworm 
#Define la imagen base que vamos a usar

RUN apt-get update && apt-get install python3-dev libgdal-dev graphviz-dev -y --force-yes 

WORKDIR /usr/src/app     
#La carpeta de trabajo dentro de la imagen de Docker. Cuando se ejecute la imagen, se va a situar en esta carpeta.

RUN pip install --upgrade pip && pip install --upgrade setuptools

COPY requirements.txt ./

RUN pip install -r requirements.txt

EXPOSE 8000
#
#Todo lo anterior ↑ solo se ejecuta la primera vez que se crea la imagen de Docker

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"] 
# CMD= Comando que ejecuta la imagen de Docker cada vez que levanta 

#RUN django-admin startproject app .
#Crea un proyecto Django llamado "app" en la carpeta de trabajo.