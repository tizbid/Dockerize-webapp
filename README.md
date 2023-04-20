### Containerize a simple python web application.

Docker is used to automate the packaging and deployment of portable, self-sufficient containers.


#### Web App
The application `main.py` is in the `src` folder and its dpendencies are contained in the 
`requirements.txt` file


The `Dockerfile` file,described in 1 build  builds app into single containers, while the
`docker-compose.yml` YAML as described in 2 builds a multi-container app.

1. #### Dockerfile
 
   * Run `docker build -t <docker-image-name>` to build the docker image template
   * Use `docker run --name <docker-container> -p 80:80 -d <docker-image-name>` to build the docker container from the image template

   For persisting data in the container use [`volumes`](https://docs.docker.com/storage/volumes/)


2. #### docker-compose.yml

   * Run `docker-compose up --build` to build application with the  associating `redis` db service . 

