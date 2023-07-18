# Django 4.2.3 LTS and Mysql with Docker

Scripts for use django, mysql, and phpmyadmin, all in Docker

1. Clone this repository.

2. Enter the folder django-mysql

```
cd django-mysql
```

3. Build the image, this will generate a image id.

```
docker build .
```

4. Create the project django with image id (first 3 characters) of step 2.

```
docker run -it --volume .:/code <image id> python -m django startproject <project name> .
```

5. Delete image of step 2

```
docker image rm <image id>
```

6. Start the containers for work.

```
docker compose up -d
```

7. If you want to see the start page of project go to http://localhost:8085/

8. If you want to use phpmyadmin go to http://localhost:8086
  - server mysql
  - user root
  - password root

9. If you want to go to container with django, use the next command.

```
docker exec -it docker-django bash
```

10. If you want to stop the containers, use the next command.

```
docker compose down
```