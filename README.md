[![LinkedIn][linkedin-shield]][linkedin-url] ![Python] ![Flask] [![MIT License][license-shield]][license-url]

# User authentication using Flask

A simple application whose intention is to experiment, apply, and characterize the various tools that **Python** offers from the frameworks [Flask](https://flask.palletsprojects.com/en/3.0.x/) & [Jinja](https://jinja.palletsprojects.com/en/3.1.x/).
This is the application of the method for the **Registration** and/or **Log-In** of a user whose data will be stored in a database deployed in [SQLAlchemy](https://www.sqlalchemy.org/).

As a reference, to deploy this mini-project I have studied the repository: [Repository](https://github.com/ondiekelijah/User-Authentication-in-Flask), from the Author: [ondiek-elijah.me](https://www.ondiek-elijah.me/tags). 

## Start Point

### Using Docker

Using the image from my [DockerHub](https://hub.docker.com/r/kevinjessid/flask-auth-system/tags):
```sh
$ docker pull kevinjessid/flask-auth-system:latest
```
Just run the a new container using the image `kevinjessid/flask-auth-system` 

https://github.com/kjfigueroa/flask-auth-system/assets/68950531/1c0e31ce-e0c3-452f-b741-ffdec226ad97

### Deploying from repo

I used [Ubuntu 20.04](https://ubuntu.com/download/server) as a host

```sh
$ sudo apt install -y python3 python3-pip
    ...
$ git clone https://github.com/kjfigueroa/flask-auth-system.git project && cd project
    ...
$ python3 -m venv micro-auth-app
$ source micro-auth-app/bin/activate
(micro-auth-app)$ cd flask-auth-system
(micro-auth-app)$ pip install -r requirements.txt
(micro-auth-app)$ python3 manage.py
(micro-auth-app)$ export FLASK_APP=routes.py
(micro-auth-app)$ export FLASK_ENV=development
(micro-auth-app)$ FLASK_DEBUG=1
(micro-auth-app)$ flask run
```
https://github.com/kjfigueroa/flask-auth-system/assets/68950531/d0fb3c01-12ba-43b7-9ffe-70bf7bc476dc

[linkedin-shield]: https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url]: https://www.linkedin.com/in/kjfigueroa/
[Python]:https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white
[Flask]: https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://raw.githubusercontent.com/kjfigueroa/flask-auth-system/main/LICENSE
