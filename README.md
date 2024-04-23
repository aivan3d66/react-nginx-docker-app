# Dockerized React App with Nginx

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Dockerfile for development:

Create a docker image by using the docker build command:

### `docker build -f Dockerfile.dev -t [image_id/image_tag] .`

Here,

- f: Path to the docker file
- t: Name and tag for the image
- . : Context for the build process

### `docker run -d -it --rm -p [host_port]:[container_port] --name [container_name] [image_id/image_tag]`

Here,

- -d: Run container in background and print container ID
- -it: Create an interactive container
- -p: Map host port to container port
- –-name: Assign a name to the container
- –-rm: Automatically remove the container when it exits.

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

## Dockerfile for production:

For production environment, we will use Nginx to serve our static files. It'll reduce the size of our app .
Create a docker image by using the docker build command:

### `docker build -t [name:tag] .`
### `docker run -d -it --rm -p [host_port]:80 --name [container_name] [image_id/image_tag]`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.