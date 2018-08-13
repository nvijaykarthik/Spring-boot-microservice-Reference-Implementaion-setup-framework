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

Download all the microservice application from repo , this is a starter setup for microservice

## It includes.

Eureka - service discovery  . this is the master app, where all other microservice will be registered to this,  discovery runs in default port 8761 (donot forget to configure/check the URL in other services) . this should be started 1st

![Eureka Dashboard](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/Eureka.JPG)


zipkin - distributed tracing , this is to trace the logs from different microservice. start this service 2nd ( donot forget to configure/check the URL in other services) default port is 9411

![Distributed Tracing](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/Zipkin-1.JPG)
<---->
![Distributed Tracing](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/Zipkin-2.JPG)

Config-server , this is to manage the configuration properties for all the microservices, currently it is configured in only spring-boot-microservice-service-one, this access the configuration service from the GIT repo -> https://github.com/nvijaykarthik/spring-boot-microservices-config-data . start this service 3rd

ZUUL - API gateway . this is to load balance or pre-intercept the services, start this service 4th. ( as it linked to eureka , the routing will be automatically handled example : if we want to access the service one , just access http://IP:port(API gateway)/service-one/.  others will be taken care automatically)

then you can start the spring boot admin , hystrix dashboard , service one . 

The Microserice is monitored in spring boot admin or Eureka.
The circute breaker configureation is monitored using the hystrix dashboard. this will give you clear picture of which serives are accessable and using the boot admin or eureka you keep an eye on whether the service is up or not

The complete flow of records/data/service are monitored in the zip kin, distributed tracing , gives the details on where it started and where it gone.

![Hystrix](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/hystrixDashoard-1.JPG)
<---->
![Hystrix](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/hystrixDashoard-2.JPG)
<---->
![Hystrix](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/hystrixDashoard-3.JPG)
<---->
![Spring boot admin](https://github.com/nvijaykarthik/Spring-boot-microservice-complete-setup-framework/blob/master/springboot-admin.JPG)
