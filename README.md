# Spring-boot-microservice-complete-setup-framework

Initial Basic reference implementation of the Microserivce using springboot .
The implementation is based on the blow architecture diagram given by spring.

![Reference implementaion microserivce distributed system](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/diagram-distributed-systems.svg)

1) Spring Boot Gateway Service using ZUUL -> https://github.com/nvijaykarthik/spring-boot-microservice-api-gateway
2) Spring boot Config service using Spring-config -> https://github.com/nvijaykarthik/spring-boot-microservice-config-server
3) Spring boot config repo via GitHub Repo -> https://github.com/nvijaykarthik/spring-boot-microservices-config-data
4) Spring boot MicroService API using ReST -> https://github.com/nvijaykarthik/spring-boot-microservice-service-one
5) Spring boot Discovery Service using Eureka -> https://github.com/nvijaykarthik/spring-boot-microservice-service-discovery
6) Spring boot  hystrix with dashboard ->https://github.com/nvijaykarthik/spring-boot-microservice-hystrix-dashboard.git
7) Spring boot distributed tracing using zipkin -> All applicaiton added with the zipkin server configuration and spring boot starter zipkin ,  https://github.com/nvijaykarthik/spring-boot-microservice-zipkin-server
8) Spring boot config dashboard using spring admin -> https://github.com/nvijaykarthik/spring-boot-microservice-admin-server
9) Spring boot client with ribbon(client side load balancer) -> https://github.com/nvijaykarthik/spring-boot-microservice-serivce-consumer
