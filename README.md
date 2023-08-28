# Configuring Python Flask sample application with github workflow on Docker

This project shows a sample Python Flask application to be build and pushed as image to docker hub. 

## Requirements

1- Created a simple sample Python Flask application.

2- DockerFile is created to run the application.

3- A workflow yaml file is created to build and push the image of this python application to Docker Hub with the user/password set as the secret of the project.


## Docker Image

Docker image is pushed into Docker Hub. Once the image is pulled from the Docker Hub, the application can be run from that image where it is hosted from port 8055. The command may look like

  docker run -d -p 8055:8055 --name FlaskTest ***/flask-python-test:<TAG_ID>
