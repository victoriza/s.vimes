# Nightwatch.js Dockerfile
Dockerfile for [Nightwatch.js](http://nightwatchjs.org/).

## Usage
Run the nightwatch tests:
```sh
docker-compose run --rm nightwatch
```

A screenshot of the test will be stored in `test/screenshots`.  
A video of the test will be stored in `test/videos`.  

Video recording is done with
[nightwatch-video-recorder](https://github.com/blueimp/nightwatch-video-recorder).

The VNC password can be changed via `VNC_PASSWORD` environment variable for the
chromedriver container.

Stop and remove the docker-compose container set:
```sh
docker-compose down -v
```

Credits
-------
Originally cloned and inspired by 
https://blueimp.net/
