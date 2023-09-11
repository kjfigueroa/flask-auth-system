[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

# User authentication using Flask

A simple application that applies the **Python web framework** (**Flask & Jinja**). The purpose is to experiment with the libraries and facilities available in the tools related to `Python`. An interesting fact is that in the libraries used there is all the necessary instrumentation to develop an application that a few years ago took several weeks of work, and with these , it is possible to deploy this type of applications or modules from any platform that requires it in a matter of hours (or days, as long as all the concepts involved are understood).

https://github.com/kjfigueroa/flask-auth-system/assets/68950531/1c0e31ce-e0c3-452f-b741-ffdec226ad97


The following are the libraries involved in the `requirement.txt` on which the **Python** environment was created:


* [alembic 1.6.5](https://alembic.sqlalchemy.org/en/latest/)
* [bcrypt 3.2.0](https://github.com/pyca/bcrypt/)
* [cffi 1.15.0](https://cffi.readthedocs.io/en/latest/)
* [click 8.0.1](https://palletsprojects.com/p/click/)
* [dnspython 2.1.0](https://www.dnspython.org/about/)
* [email-validator 1.1.3](https://github.com/JoshData/python-email-validator)
* [Flask 2.0.1](https://pypi.org/project/Flask/)
* [Flask-Bcrypt 0.7.1](https://github.com/maxcountryman/flask-bcrypt)
* [Flask-Login 0.5.0](https://github.com/maxcountryman/flask-login)
* [Flask-Migrate 3.1.0](https://github.com/miguelgrinberg/flask-migrate)
* [Flask-SQLAlchemy 2.5.1](https://github.com/pallets-eco/flask-sqlalchemy/)
* [Flask-WTF 0.15.1](https://github.com/wtforms/flask-wtf/)
* [greenlet 1.1.1](https://greenlet.readthedocs.io/en/latest/)
* [idna 3.2](https://github.com/kjd/idna)
* [itsdangerous 2.0.1](https://itsdangerous.palletsprojects.com/en/2.1.x/)
* [Jinja2 3.0.1](https://palletsprojects.com/p/jinja/)
* [Mako 1.1.5](https://www.makotemplates.org/)
* [MarkupSafe 2.0.1](https://github.com/pallets/markupsafe/)
* [pycparser 2.20](https://github.com/eliben/pycparser)
* [python-dateutil 2.8.2](https://github.com/dateutil/dateutil)
* [python-editor 1.0.4](https://github.com/fmoo/python-editor)
* [six 1.16.0](https://github.com/benjaminp/six)
* [SQLAlchemy 1.4.23](https://www.sqlalchemy.org/)
* [Werkzeug 2.0.1](https://pypi.org/project/Werkzeug/)

I took a great reference understanding the way to code, and the structure of this small project from this [Repository](https://github.com/ondiekelijah/User-Authentication-in-Flask), and I leave a link from the same author of which there is a very good bibliography to start swimming in these topics [ondiek-elijah.me](https://www.ondiek-elijah.me/tags). 

## Start Point

### Using Docker
To deploy the app is soo straightforward, for this, I had a simple virtual machine like below:
```
DISTRIB_RELEASE=18.04
DISTRIB_CODENAME=bionic
DISTRIB_DESCRIPTION="Ubuntu 18.04.4 LTS"
```
Using the following version of `Docker`:
```
$ apt list docker
Listing... Done
docker/bionic 1.5-1build1 amd64
$ docker --version
Docker version 24.0.2, build cb74dfc 
```

#### How to:
And, once the project image has been downloaded from [DockerHub](https://hub.docker.com/r/kevinjessid/flask-auth-system/tags):
```
$ docker pull kevinjessid/flask-auth-system:latest
```
Just run the application as follows:
```
$ docker run -d -it --name test -p 8080:5000 kevinjessid/flask-auth-system
```

### From the Repo

It is possible to skip this step if you already have the necessary packages.
Following, Python and Python-pip are installed:
```
$ sudo apt install -y python3 python3-pip
```
Clone the repo and prepare a virtual environment for the isolated management of python libraries:
```
$ git clone https://github.com/kjfigueroa/flask-auth-system.git 
    ...
$ python3 venv -m env
$ source env/bin/activate
(env)$ cd flask-auth-system
(env)$ pip install -r requirements.txt
(env)$ python3 manage.py
```
Finally, the variables are exported, so that the system recognizes the application and can deploy it:
```
(env)$ export FLASK_APP=routes.py
(env)$ export FLASK_ENV=development
(env)$ FLASK_DEBUG=1
(env)$ flask run
```
If it's from a virtual machine, it is necessary to indicate the exit from any point on the inet interface:
```
(env)$ flask run --host=0.0.0.0
```
<br />
<div align="center">
Thanks for reading!
</div>

[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://raw.githubusercontent.com/kjfigueroa/flask-auth-system/main/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/kjfigueroa/
