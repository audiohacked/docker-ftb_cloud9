# Feed-The-Beast Cloud 9 (Minecraft 1.7.10) in a Docker Container
To pull the image:
```
docker pull audiohacked/ftb_cloud9:1.3.0
```
*Optional*: Run data container:
```
docker run --name ftb_cloud9_data audiohacked/ftb_cloud9:1.3.0 true
```

Then, run the server container:
```
docker run --detach --interactive --tty \
    --name ftb_cloud9 \
    --volumes-from ftb_cloud9_data \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/ftb_cloud9:1.3.0
```
