# Configuring Python Flask sample application with github workflow on Docker

This project shows a sample Python Flask application to be build and pushed as image to docker hub. 

## Requirements

1- Created a simple sample Python Flask application.

2- DockerFile is created to run the application.

3- A workflow yaml file is created to build and push the image of this python application to Docker Hub with the user/password set as the secret of the project.


## Docker Image

Docker image is pushed into Docker Hub. Once the image is pulled from the Docker Hub, the application can be run from that image where it is hosted from port `8055`. This port can be changed within `flaskApplicaiton.py` file as:

```app.run(debug=True, host='0.0.0.0', port=8055)```

After the image is pulled to local repository, it can be run as the command may show:

```docker run -d -p 8055:8055 --name FlaskTest ***/flask-python-test:```_**<TAG_ID>**_

`***` indicates the repository user.

`<TAG_ID>` indicates the image tag which is the github_sha ID.
