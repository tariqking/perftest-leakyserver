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

You can then view these dashboards - 
* [App Stats Dashboard](http://localhost:3000/d/17kOE7Onk/spring-boot-app?orgId=1&refresh=30s&from=now-15m&to=now)
* [Prometheus Stats Dashboard](http://localhost:3000/d/UDdpyzz7z/prometheus-stats?orgId=1&refresh=5s&from=now-15m&to=now)
