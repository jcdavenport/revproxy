# revproxy
nginx reverse-proxy for accessing Docker containers from web browser.


INSTRUCTIONS:

*First, install docker-compose as a container on RancherOS according to: https://docs.docker.com/compose/install/#install-compose.

#git clone into rancherOS
alias git="docker run -ti --rm -v ${HOME}:/root -v $(pwd):/git bwits/docker-git-alpine"

git clone https://github.com/jcdavenport/revproxy.git

docker build -t reverseproxy ./path/to/directory/with/dockerfile/and/nginx.conf


#to run everything:
docker-compose up -d



##to access each gui server container

#WebUI container management
http://localhost:8080

#Alpine noVNC webserver
http://localhost:8081

#Kali desktop web interface
http://localhost:8082
