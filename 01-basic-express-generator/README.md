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
* runs the application (`app/bin/www`) and visit the application on http://localhost:3000

Dockerfile instructions to use: `FROM`, `RUN`, `ADD`/`COPY`, `CMD`, `EXPOSE`, `WORKDIR`
Docker commands: `run`, `build`

3. Retrieve information from the image, container

* describe the different layers of the Docker image built previously
* inspect the container (networks, volumes, ports, ...)
* find the logs of the container currently running

Docker commands: `inspect`, `history`, `logs`
