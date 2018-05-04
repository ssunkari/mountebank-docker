# mountebank-docker
A docker image for [mountebank](http://www.mbtest.org/).

### Build Docker Image
    docker-compose build

## Run
Run the image as follows replacing PORT with the port of your imposter(s)

    docker-compose up or docker-compose up -d

Alternatively, use --net=host to use the host network and avoid need to specify all the imposter ports upfront

    docker run --net=host -t [Tag]
