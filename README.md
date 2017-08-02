# Payara Micro test
An simple aplication to know how payara micro works

[![Build Status](https://travis-ci.org/robsonbittencourt/payara-micro-test.svg?branch=master)](https://travis-ci.org/robsonbittencourt/payara-micro-test)  [![Docker Stars](https://img.shields.io/docker/stars/robsonbittencourt/payara-micro-test.svg)](https://hub.docker.com/r/robsonbittencourt/payara-micro-test/)  [![Docker Pulls](https://img.shields.io/docker/pulls/robsonbittencourt/payara-micro-test.svg)](https://hub.docker.com/r/robsonbittencourt/payara-micro-test/)  [![image-size](https://images.microbadger.com/badges/image/robsonbittencourt/payara-micro-test.svg)](http://microbadger.com/images/robsonbittencourt/payara-micro-test)

>Payara Micro enables you to run WAR files from the command line without any application server installation.

## How to run with Docker
This project have a image in DockerHub. It's just a test, with the goal of demonstrating use with Docker.

```bash
docker run -d -p 8080:8080 --name=payara-micro robsonbittencourt/payara-micro-test
```

## How to build and run manually
Download Payara Micro jar in the [project download page](https://www.payara.fish/downloads).

```bash
## Build the application
mvn clean package

## Create UberJar with embedded Payara Micro
java -jar PATH_TO_PAYARA_MICRO_JAR --deploy target/payara-micro-test.war --outputUberJar payara-micro-test.jar

## Run generated UberJar
java -jar payara-micro-test.jar
```

Acess the following address to see the result
http://localhost:8080/payara-micro-test/rest/calculate/doubleOf/10

## Meta
Robson Bittencourt - @rluizv - robson.luizv@gmail.com

Distributed under the MIT license. See [LICENSE](LICENSE) for more information.

https://github.com/robsonbittencourt/payara-micro-test