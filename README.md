# Sharelatex on lab2c server cluster
## Instructions
See http://10.8.6.22:88/yang/clusterhowto/blob/master/maintenance/docker.md for latest instructions.
The following is out of date.

How to start the sharelatex server from refresh?
```shell
docker-compose up
```
How to stop the sharelatex server
```shell
docker-compose stop # not remove the container
```
How to re-start the sharelatex server
```shell
docker-compose start
```
How to grant a user as admin
```shell
$ docker exec -it mongo mongo
> use sharelatex
switched to db sharelatex
> db.users.update({email: 'admin@example.com'}, {$set: {isAdmin: true}})
```
How to add a new user?

Login to aadmin user, and use web panel to create a normal user.
