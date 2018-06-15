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

### Some Example tests failed
There are two provided tests:
app-success-example.js (that points to the app)    OK  
google-fail-example.js (that points to google.com) KO  
It's a test from http://nightwatchjs.org/ for an "old" version of Google, it shows how nicely you spot a broken functionality.

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

Headless Chrome Project
https://developers.google.com/web/updates/2017/04/headless-chrome

Nightwatch.js Project
http://nightwatchjs.org/

