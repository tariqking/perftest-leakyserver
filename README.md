# Leaky Web Server Exercise

### Pre-requisites

The following need to be installed on your system:

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)
* [JMeter](https://jmeter.apache.org/download_jmeter.cgi)
* [JMeter Prometheus Plugin](https://github.com/johrstrom/jmeter-prometheus-plugin/releases)

### Build and run the project

Build the project using the following build script

```shell
$ ./bnd.sh
```

### Grafana

* [Login to grafana](http://127.0.0.1:3000/login) with these credentials

```
user: admin
pass: admin
```

* Skip updating password
* [Add a datasource at this link](http://127.0.0.1:3000/datasources) and fill in the details below

```
type: Prometheus
URL: http://prometheus:9090
```
* Click Save and Test
* Visit [the explore tab](http://127.0.0.1:3000/explore?orgId=1&left=%5B%22now-5m%22,%22now%22,%22Prometheus%22,%7B%22refId%22:%22A%22,%22exemplar%22:true,%22expr%22:%22jvm_memory_committed_bytes%7B%7D%22%7D%5D) to explore the metrics being captured
