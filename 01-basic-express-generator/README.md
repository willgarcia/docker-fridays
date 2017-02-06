# Instructions

1. Create a Dockerfile that:

* installs node version 0.10.* from an existing image available on Docker hub
* run the container with node. the application is not installed at this stage.
* find the OS distribution and version inside the container (cat /etc/*release*)


* creates a directory /src inside the container
* installs express-generator (npm install express-generator)
* makes a copy of the current code directory in the container (/src)

* runs the application (app/bin/www)
* find the logs for the container

Dockerfile instructions to use: FROM, RUN, ADD/COPY, CMD, EXPOSE, WORKDIR
Docker commands: run, exec, build, inspect, history, logs

2. Build an image called basic-express-generator from the previous Dockerfile

3. Run the image to create a container and access the application on http://localhost:3000
