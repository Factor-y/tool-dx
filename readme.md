# tool-dx

The swiss army knife of HCL DX development tooling. Built on the experience at Factor-y S.r.l. 

## Help reference

### Create the image and tag it
    docker build . -t thin-client
### List images created
    docker images
### Clean 'dangling' images
    docker image prune
### Rename an image (tag it)
    docker tag thin-client:latest fy-docker-private-nexus.factor-y.com/fy/dx/thin-client:9.5.5
### Push image to repo
    docker push fy-docker-private-nexus.factor-y.com/fy/dx/thin-client:9.5.5
### Run entrypoint with parameters
Options:

    -i: keep stdin open
    -t: allocate pseudo tty
    --rm: remove container on exit
    [args]: arguments for entrypoint if defined / command to execute if no entrypoint is defined

    docker run -it --rm thin-client -port 10033 -user wpsadmin -password wpsadmin -host 10.0.2.15