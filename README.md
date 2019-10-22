# Getting Started

Sample project to test a Traefik load balancer backed by Consul Catalog.
One Spring Boot application is registering a boot time to Consul and should be available at `http://localhost/{PATH_PREFIX}`.
See the `.env` file.

### Setup

```shell script
$ docker-compose -f docker/backing-services/consul-traefik.yml up -d
$ ./gradlew build
$ docker build -f docker/prod/Dockerfile -t demo-consul build/libs
$ docker run --env-file .env --network host -t demo-consul
```

### Reference Documentation
For further reference, please consider the following sections:

* [Official Gradle documentation](https://docs.gradle.org)
* [Spring Boot Gradle Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.1.9.RELEASE/gradle-plugin/reference/html/)
* [Spring Configuration Processor](https://docs.spring.io/spring-boot/docs/2.1.9.RELEASE/reference/htmlsingle/#configuration-metadata-annotation-processor)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.1.9.RELEASE/reference/htmlsingle/#boot-features-developing-web-applications)
* [Spring Boot DevTools](https://docs.spring.io/spring-boot/docs/2.1.9.RELEASE/reference/htmlsingle/#using-boot-devtools)
* [Dockerize Spring Boot](https://spring.io/guides/gs/spring-boot-docker/)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)

### Additional Links
These additional references should also help you:

* [Gradle Build Scans – insights for your project's build](https://scans.gradle.com#gradle)

