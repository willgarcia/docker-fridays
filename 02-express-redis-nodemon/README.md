# Instructions

1. Build an image with a defined version of node

* installs node version 0.10.* from an existing image available on Docker hub
* run the container with node. the application is not installed at this stage.
- verify the version of node (`node -v`)
- find the OS distribution and version inside the container (`cat /etc/*release*`)

Dockerfile instructions to use: `FROM`
Docker commands: `run`, `exec`, `build`

2. Package the current application within the same image and rebuild it

* create a directory `/src` inside the container
* install express-generator (`npm install express-generator`)
* makes a copy of the current code directory in the container (`/src`)
* expose the port 3000 so your application can be accessible by `localhost:3000`
* runs the application (`npm start`)

Dockerfile instructions to use: `FROM`, `RUN`, `ADD`/`COPY`, `CMD`, `EXPOSE`, `WORKDIR`
Docker commands: `run`, `build`

3. Use docker-compose to link the container/image to redis. This applications has redis dependency

  * build the docker image
  * map the volume in the container to the app
  * map the port 3000 the app is running to another available port e.g 5000
  * link the container to redis container


  docker-compose instructions to use: `build`, `volumes`, `ports`, `links`
  docker-compose commands: docker-compose up
