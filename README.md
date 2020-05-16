# Microservices Spring Cloud
A small web application to demonstrate the concept of Spring Microservices using Spring Cloud and Netflix Components

### Prerequisites

What things you need to install before starting

* JDK 1.8
* Eclipse & Embedded Maven
* PostMan - (https://www.postman.com/downloads/)
* Git Client - (https://git-scm.com/)
* Rabbit MQ - (https://www.rabbitmq.com/install-windows.html)
* Zipkin - (https://zipkin.io/pages/quickstart)

## Getting Started

These instructions will help you to get your project up and running on your local machine for development and testing purposes. The application is build on top of Spring Boot (https://spring.io/projects/spring-boot) providing a runtime container. 

## Main Features

* Netflix Eureka - Naming Server
* Netflix Zuul- API Gateway
* Spring Cloud Config - Config Server
* Hystrix - Fault Tolerance
* Feign - Rest Client
* Ribbon - Client Side Load Balancing
* Spring Cloud Sleuth - Distributed Tracing - Unique Id for request
* Zipkin - Distributed Tracing Server
* RabbitMQ - Message Queue
* Spring Cloud Bus - Refresh config update on all instances

## How to use git ##

All sources are available as public at https://github.com/sumanth25/microservices-spring-cloud
To use git to get repository contents run the following git command:

```
#!bash
git clone https://github.com/sumanth25/microservices-spring-cloud.git
```

## How to use RabbitMQ and Zipkin together ##

Install RabbitMQ as a service in windows/mac and download Zipkin jar
Use the below commands:

```
set RABBIT_URI=amqp://localhost
java -jar zipkin-server-2.7.0-exec.jar

Additionally, if you like to see RabbitMQ admin:
* Go to Program Files -> RabbitMQ Server -> rabbitmq_server-3.8.3 -> sbin
* Run cmd: rabbitmq-plugins enable rabbitmq_management
* In browser, go to (http://localhost:15672/) and login as default user:guest;pwd:guest
```

## Ports and URL's

|     Application       |     Port          |     URL     |
| ------------- | ------------- | ------------------------ |
| Netflix Eureka Naming Server | 8761 | (http://localhost:8761/eureka/) |
| Netflix Zuul API Gateway Server | 8765 | (http://localhost:8765/currency-conversion-service/currency-converter-feign/from/USD/to/INR/quantity/1000) | 
| Spring Cloud Config Server | 8888 | (http://localhost:8888/limits-service/default) |
| Limits Service | 8282, 8283, ... | (http://localhost:8080/limits)* |
| Currency Exchange Service | 8000, 8001, 8002, ..  | (http://localhost:8000/currency-exchange/from/USD/to/INR/) |
| Currency Conversion Service | 8100, 8200, 8300, ... | (http://localhost:8100/currency-converter/from/USD/to/INR/quantity/1000) |
| Zipkin Distributed Tracing Server | 9411 | (http://localhost:9411/zipkin/) |

*Default port 8080 as no port is specified in dev profile as users are expected to run multiple instances with ports (8282,8283) in local Run Configurations of Eclipse/IntelliJ

## Deployment

* Use jenkins job or batch scripts to automate start/stop. You can manually start it with java -jar currency-conversion-service 0.0.1.jar. 


## Authors

* **Sumanth Sudeendra**  - *Initial work* - (https://github.com/sumanth25/microservices-spring-cloud)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Thank You In28Minutes! - (https://www.udemy.com/course/microservices-with-spring-boot-and-spring-cloud/)
