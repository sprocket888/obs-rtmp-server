# obs-rtmp-server

Build the docker container from the Docker file
`docker build -t <Tag of your choice> .`

Now run the built container
`docker run --rm -d -p 1935:1935 -v <FULL local path>:/opt/local <Tag used in build>`

If you don't have any local files to stream you can omit the `-v <FULL local path>:/opt/local`
the --rm cleans up when the container is stopped
the -d runs it as a dameon
the -p is important because it will open up a listening port on the Host machine at 1935
