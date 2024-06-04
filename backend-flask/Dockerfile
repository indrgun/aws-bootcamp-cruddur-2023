FROM python:3.10-slim-buster

# Inside Container
# make a new folder inside container
WORKDIR /backend-flask

# Outside Container -> Inside Container
# this contains the libraries that want to install
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# means everything in the current directory
COPY . .

# Set Environment Variables (Env Vars)
# Inside Container and will remain set when the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]