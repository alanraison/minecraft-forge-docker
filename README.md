minecraft-forge-docker
======================

A docker container for a minecraft forge server.

As with the base `alanraison/minecraft` container, a `eula.txt` file must be added to the workdir, with the contents
```
eula=true
```
to indicate acceptance of the End User License Agreement.

This can be achieved by placing the file in a directory with the Dockerfile
```
FROM alanraison/minecraft-forge:latest
COPY eula.txt ./
```

Then build the container with

```
docker build -t minecraft-forge
docker run -d minecraft-forge
```
