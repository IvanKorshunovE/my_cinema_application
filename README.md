# Cinema API

API service for cinema management

## Installing using GitHub (macOS)

- `git clone https://github.com/IvanKorshunovE/my_cinema_application`
- `cd my_cinema_application`
- `python -m venv venv`
- `source venv/bin/activate`
- `pip install -r requirements.txt`
- `set POSTGRES_HOST=<your db hostname>`
- `set POSTGRES_DB=<your db name>`
- `set POSTGRES_USER=<your db user>`
- `set POSTGRES_PASSWORD=<your db password>`
- `set SECRET_KEY=<your secret key>`


After you have done everything before:
- `python manage.py migrate`
- `python manage.py runserver`

How to run this in docker:
- `docker-compose build`
- `docker-compose up`

To create a superuser in Django within a Docker container, you can follow these steps:
- First, identify the name of the container running your Django application. You can use the docker ps command to list all running containers and find the container name associated with your Django app.
- Once you have the container name, you can use the docker exec command to execute commands inside the container. The command should be structured as follows:
- `docker exec -it <container_name> python manage.py createsuperuser`

Endpoints:
- create user via /api/user/register/
- get access token via /api/user/token/

Features
- JWT authenticated 🔒
- Admin panel /admin/
- Creating movies with genres, actors
- Creating cinema halls
- Adding movie sessions
- Managing orders and tickets
- Filtering movies and movie sessions
