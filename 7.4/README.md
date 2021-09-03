# docker-apache-proxy Web Service

A Docker container to provide a web service that uses a proxy server to process applications written in PHP.

The container runs an instance of Apache Web server to display and retrieve data through standard web protocols. For processing PHP files, this container looks for a PHP service container like [llslim/phpfpm](https://hub.docker.com/repository/docker/llslim/phpfpm) to use as a proxy. 

This Apache Web Server container is intended to work as a part of an orchestrated bundle of web, database and mail service docker containers to provide a platform for developing and testing complete web applications on a laptop or desktop. The goal is to have an easy and quick way to start a web application using the docker-compose utility. For more information on how the platform is implemented see the [docker-phpweb](https://github.com/llslim/docker-phpweb) repository.

Security measures against malicious attacks is not a high priority for this container. Again, the intent of this container is for testing and development web applications on a personal laptop or desktop.  Using it in a production environment is NOT recommended.

# Logs
Docker can display the logs of this container when we run the following on the command line:

`docker logs <container_name or ID>`.

## Base Container
The [Offical PHP Container](https://hub.docker.com/_/php/) is used as a base container.
