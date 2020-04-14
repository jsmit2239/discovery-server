discovery-server
==============

Eureka is a REST (Representational State Transfer) based service that is primarily used in the AWS cloud for locating services for the purpose of load balancing and failover of middle-tier servers.

At Netflix, Eureka is used for the following purposes apart from playing a critical part in mid-tier load balancing.

* For aiding Netflix Asgard - an open source service which makes cloud deployments easier, in  
    + Fast rollback of versions in case of problems avoiding the re-launch of 100's of instances which 
      could take a long time.
    + In rolling pushes, for avoiding propagation of a new version to all instances in case of problems.

* For our cassandra deployments to take instances out of traffic for maintenance.

* For our memcached caching services to identify the list of nodes in the ring.

* For carrying other additional application specific metadata about services for various other reasons.

(From https://github.com/Netflix/eureka/blob/master/README.md)

Technologies
------------

- Java 8
- Maven
- Spring Boot
- Spring Cloud
- Eureka

How To Run
----------

Requirements 
- [Java 8](https://java.com/en/download/help/download_options.xml)
- [Maven](https://maven.apache.org/install.html)

Run
```
mvn spring-boot:run
```
at the project root to start the discovery service.

Default Port
-------------------
- **discovery-server**: 8761
