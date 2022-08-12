# utz-thesis-docker

This is the docker setup for the software used in my thesis. 

## Usage

To build the application and run it locally generate a docker container and run it:

```bash
# build docker container -> this may take some time!
$ docker-compose build

# start the container
$ docker-compose up
```
Depending on your Docker configurations you may have to add `sudo` before the comands

The application will be reachable under  	[http://localhost:8100](http://localhost:8100) as long as the container is up. 

## Clean up

After testing the application remember to remove the docker container to prevent cluttering your system:

```bash
# check status 
$ docker-compose ps

# remove the container
$ docker-compose rm thesis
```
before removing the containter the status should be:
```bash
$ docker-compose ps

Name                 Command               State         Ports
---------------------------------------------------------------
thesis   docker-entrypoint.sh npm start    Exit 0 
```

after removal the container should be gone:
```bash
$ docker-compose ps

Name Command State Ports
------------------------
```


## Application Information

For more information on the application refer to the README within the thesis folder.
