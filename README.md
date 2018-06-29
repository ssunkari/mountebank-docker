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

the imposters loaded automatically, the multi stage docker file validates the functionality of mountebank in the build stage by running automated tests to make sure imposters are fully functional and can be extended to verify javascript injections work for your imposters. Newman cli is used for running automated tests

    npx newman run /postman.json --global-var "mountebank=localhost" --global-var "port=2525"
  
