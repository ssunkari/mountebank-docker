# Mountebank Docker Image

Provides [mountebank](http://www.mbtest.org/).

## Supported tags and respective `Dockerfile` links
 * [`latest` (Dockerfile)](https://github.com/ssunkari/mountebank-docker/blob/master/Dockerfile)

## ssunkari/mountebank:latest

Installs the latest version of mountebank and exposes port 2525 ready for
configuration and testing.

Running mountebank is achieved by:

    docker run -p 2525:2525 -d ssunkari/mountebank

and then visiting [localhost:2525](http://localhost:2525).

If you wish to load your imposters automatically, mount your imposters as a
volume and bind the necessary ports:

    docker run \
        -v ./templates:/imposters \
        [-p IMPOSTER_1_PORT:IMPOSTER_1_PORT ...] \
        -p 2525:2525 \
        -d ssunkari/mountebank \
        --configfile /imposters/imposters.ejs --allowInjection
