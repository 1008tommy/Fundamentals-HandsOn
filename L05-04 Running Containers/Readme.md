# L05-04

Type the following Docker commands:

## Pull and run a Nginx server
## -p is port, --name is the name of the container, -d will run it in the background, this allow
## us to use the terminal for other commands while the container runs in the background
    docker run -d -p 8080:80 --name webserver nginx

## List the running containers

    docker ps

## List the images

    docker images

## Attach to the container

    docker container exec -it  webserver bash  

Exit by typing

    exit

## Stop the container
## use docker ps -a to see the stopped webserver
    docker stop webserver

## Remove the container from memory
## docker ps -a will not show the webserver
    docker rm webserver

## Remove the image
## Once removed use docker images to check if it is removed, note that the removed name is the 
## image name, not the container name
    docker rmi nginx