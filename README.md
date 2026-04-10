# ⚙️ GMS Configuration Repository

This repository contains the centralized configuration files for the **Greenhouse Management System (GMS)** microservices project.

The configurations are used by Spring Cloud Config Server to manage all microservices in a centralized and consistent way.

---

## 📌 Project Overview

GMS is a microservice-based system that includes:

- User Service
- Zone Service
- Sensor Service
- Crop Service
- Automation Service
- API Gateway
- Eureka Server

All services load their configuration from this repository using **Spring Cloud Config Server**.

---

## 🗂️ Repository Structure

## GMS_config_repo/
## │
## ├── user-service.yml
## ├── zone-service.yml
## ├── sensor-service.yml
## ├── crop-service.yml
## ├── automation-service.yml
## ├── api-gateway.yml
## ├── eureka-server.yml
## └── application.yml


---

## ⚙️ How It Works

1. Config Server reads YAML files from this repository
2. Each microservice requests its configuration at startup
3. Configurations are applied dynamically without hardcoding

---


## 🌱 Example Configurations


## 👤 user-service.yml

server:
  port: 8081

spring:
  application:
    name: user-service

eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/



 ## 🌱 zone-service.yml

 server:
  port: 8082

spring:
  application:
    name: zone-service

eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/



## 🌡 sensor-service.yml

server:
  port: 8085

spring:
  application:
    name: sensor-service

eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/



## 🌾 crop-service.yml

server:
  port: 8084

spring:
  application:
    name: crop-service

eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/



## 🤖 automation-service.yml

server:
  port: 8083

spring:
  application:
    name: automation-service

eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/



## 🌐 api-gateway.yml

server:
  port: 8080

spring:
  application:
    name: api-gateway

eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/



## 🧭 eureka-server.yml

server:
  port: 8761

spring:
  application:
    name: eureka-server

eureka:
  client:
    register-with-eureka: false
    fetch-registry: false



---



## 🚀 Technologies Used
Spring Boot
Spring Cloud Config
Netflix Eureka Server
Spring Cloud Gateway
Microservices Architecture
YAML Configuration Management



---



## 🎯 Purpose of This Repository

✔ Centralized configuration management
✔ Avoid hardcoding configuration in services
✔ Easy maintenance and updates
✔ Supports microservice scalability
✔ Dynamic configuration loading via Config Server



---



## 👨‍💻 Author

Sithumini Silva



---



## 📌 Important Note

All YAML files must match the exact spring.application.name of each microservice.

Config Server must be running before starting microservices.


---






