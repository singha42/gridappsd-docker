# gridappsd-docker

## Requirements
 - docker version 1.09.0 or higher
 - docker-compose version 1.16.1 or higher
 - user must be a member of the docker group to run docker without sudo
```
 sudo usermod -a -G docker $USER
```

## Clone or download the repository
```
  git clone https://github.com/GRIDAPPSD/gridappsd-docker
  cd gridappsd-docker
```

## Start the docker container services
```
./run.sh
```
The run.sh does the folowing
 -  download the mysql dump file
 -  download the blazegraph data
 -  download the applications
 -  download the services
 -  start the docker containers
 -  ingest the blazegraph data

## Start gridappsd

Connect to the running gridappsd container
```
user@foo>docker exec -it gridappsddocker_gridappsd_1 bash

```
Now we are inside the executing container
```
root@737c30c82df7:/gridappsd# ./gridappsd.run.sh

```
Open your browser to http://localhost:8080/ieee8500

Click the triangle in the top right corner to have a simulation run.

## Exiting the container and stopping the containers

```
Use Ctrl+C to stop gridappsd from running
exit
./stop.sh
```

## Restarting the containers
```
./run.sh
```

## Future enhancements    
  -  open a web browser to the viz container http://localhost:8080
