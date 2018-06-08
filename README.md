# Nightwatch.js Dockerfile
Dockerfile for [Nightwatch.js](http://nightwatchjs.org/).

## Usage
Run the nightwatch tests:
```sh
docker-compose run --rm nightwatch
```

A screenshot of the test will be stored in `test/screenshots`.  
A video of the test will be stored in `test/videos`.  
A Nightwatch log will be shown on the console.

Stop and remove the docker-compose container set:
```sh
docker-compose down -v
```

## FAQ

### Permission denied for videos/screenshots folders
If you get a permission error for the videos/screenshots folders, make sure they
are writable for the nightwatch process:

```sh
mkdir -p test/screenshots test/videos
chmod 777 test/screenshots test/videos
```

Credits
-------
Originally cloned and inspired by 
https://blueimp.net/
