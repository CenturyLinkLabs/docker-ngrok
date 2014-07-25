ngrok for Docker
============
Heavily leveraged [fnichol/ngrok](https://registry.hub.docker.com/u/fnichol/ngrok/), but made some changes to the Dockerfile including using the ADD to get the zip rather than installing and running curl. Also leveraging the official busybox ubuntu 14.04 image. Changed from an ENTRYPOINT to a CMD to force use of environemental variables and removed the EXPOSE 4040.

Example usage:
`docker run --rm --name ngrok -e "HTTP_PORT=192.168.0.100:8080" centurylinklabs/ngrok`

Valid environmental variables are: `HTTP_PORT` and `HTTPS_PORT`

View the docker logs for the running container to see the URL to use to access.

Detailed instructions [here](https://ngrok.com).  


