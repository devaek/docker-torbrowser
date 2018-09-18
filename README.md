# Tor Browser - Docker Project #

This project is providing an ephemeral image optionally anonymous for web browsing.

## Build image from Dockerfile ##

```
$ git clone https://github.com/devaek/docker-torbrowser.git
$ cd docker-torbrowser
$ sudo docker build -t devaek/torbrowser .
```

or 

```
$ sudo docker build github.com/devaek/docker-torbrowser
```

## Browse web ##

Start torbrowser like so:
`sudo docker run -i -t --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix:ro devaek/torbrowser`

Or start iceweasel like so:

`sudo docker run -i -t --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix:ro devaek/torbrowser iceweasel`

_add `-v /tmp/Downloads:/home/anon/Downloads` if you do not wish to save downloads_

Pressing CTRL+C or closing the browser window will stop the container.
