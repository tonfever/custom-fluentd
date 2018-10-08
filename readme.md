# Run a fluentd container to grab log files to send to Elasticsearch

## Commands

### Build a custom docker image

docker build -t custom-fluentd:latest ./

docker build -t akscr007.azurecr.io/custom-fluentd:latest ./

### Run a container

docker run -it --rm --network=elastic-net --name=custom-docker-fluent-logger -v <LOG_PATH>:/fluentd/log -v hellovol:/logback custom-fluentd:latest


