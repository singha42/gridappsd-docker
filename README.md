# gridappsd-docker

## Start the docker container services

    ./run.sh

The run.sh does the folowing
 -  download the mysql dump file
 -  download the blazegraph data
 -  download the applications
 -  download the services
 -  start the docker containers
 -  ingest the blazegraph data


## start gridappsd

Currently the default container for gridappsd does not start automatically so
the following must be run.

````
user@foo>docker exec -it gridappsddocker_gridappsd_1 bash

# Now we are inside the executing container
root@737c30c82df7:/gridappsd# ./gridappsd.run.sh
````

Open your browser to http://localhost:8080/ieee8500

Click the triangle in the top right corner to have a simulation run.

## Close and remove the containers

    docker-compose down

### Future enhancements    
  -  open a web browser to the viz container http://localhost:8080
