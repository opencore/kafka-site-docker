# kafka-site-docker
A httpd container configured so that the Kafka documentation page can be served.

## Building
Clone repo, change into directory and run

docker build . -t <imagename>

## Running
After building run the following from a directory into which the kafka-site repository was cloned:

docker run -dit --name kafka-site -p 8080:80 -v "$PWD":/usr/local/apache2/htdocs/ <imagename>

Site should now be available on port 8080.