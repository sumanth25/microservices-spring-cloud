# Microservices Spring Cloud
A small web application to demonstrate the concept of Spring Microservices using Spring Cloud and Netflix Components

### Prerequisites

What things you need to install before starting

```
JDK 1.8
Eclipse & Embedded Maven
PostMan
Git Client - (https://git-scm.com/)
Rabbit MQ - (https://www.rabbitmq.com/install-windows.html)
Zipkin - (https://zipkin.io/pages/quickstart)
```
## Getting Started

These instructions will help you to get your project up and running on your local machine for development and testing purposes. The application is build on top of Spring Boot (https://spring.io/projects/spring-boot) providing a runtime container. 

## How to use git ##

All sources are available as public at https://github.com/sumanth25/microservices-spring-cloud
To use git to get repository contents run the following git command:

```
#!bash
git clone https://github.com/sumanth25/microservices-spring-cloud.git
```
## Main Features

* Netflix Eureka (Naming Server)
* Netflix Zuul (API Gateway)
* Spring Cloud Config (Config Server)
* Hystrix (Fault Tolerance)
* Feign (Rest Client)
* Ribbon (Client Side Load Balancing)
* Spring Cloud Sleuth (Distributed Tracing - Unique Id for request)
* Zipkin (Distributed Tracing Server)
* RabbitMQ (Message Queue)
* Spring Cloud Bus (Refresh config update on all instances)

## Ports

|     Application       |     Port          |
| ------------- | ------------- |
| Netflix Eureka Naming Server | 8761 |
| Netflix Zuul API Gateway Server | 8765 |
| Spring Cloud Config Server | 8888 |
| Limits Service | 8282, 8283, ... |
| Currency Exchange Service | 8000, 8001, 8002, ..  |
| Currency Conversion Service | 8100, 8200, 8300, ... |
| Zipkin Distributed Tracing Server | 9411 |

## Deployment

* Use jenkins job or batch scripts to automate start/stop. You can manually start it with java -jar registration-0.1.0.jar. 


## Authors

* **Sumanth Sudeendra**  - *Initial work* - (https://github.com/sumanth25/microservices-spring-cloud)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thank You In28Minutes - (https://www.udemy.com/course/microservices-with-spring-boot-and-spring-cloud/)!
