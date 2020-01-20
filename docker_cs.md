#### Docker Cheatsheet

# Architect. Runs on top of cgroups, fs overlays and namespaces

Client <$docker>           Docker Host  <daemon: containers and images>             Registry:images <url>

-a attach

container layer: r/w
images layer: shaA
image  layer: shaB
image  layer: shaC
....etc.....

# images
common url's:


docker committ    (freeze present container}
docker build   (assemble image)


# Dockerfile
each cmd makes a  new sha layer

# FS
docker cp (copy to and from container)
docker -v (/localFS:/containerPath    or createdMount:containerPath)

# linking

connecting two containers together

docker run --link <containerName|Id>:<alias> <newContainerImageToRun>  <cmd>
