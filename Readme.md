# Run Jenkins Using Docker

## Build Jenkins Image

`docker build -it myjenkins .`

## Run Jenkins in Docker

`docker run --rm -d -it -u root -p 8080:8080 -v $(pwd)/jenkins:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/usr/bin/docker myjenkins`
