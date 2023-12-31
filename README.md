# Manage Resources Reservation Application
# Getting Started
## 📚Prerequisite
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![SpringBoot](https://img.shields.io/badge/Spring%20Boot-6DB33F.svg?style=for-the-badge&logo=Spring-Boot&logoColor=white)
![SpringSecurity](https://img.shields.io/badge/Spring%20Security-6DB33F.svg?style=for-the-badge&logo=Spring-Security&logoColor=white)
![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white)
![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJIDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)
![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)
![Consul](https://img.shields.io/badge/Consul-F24C53.svg?style=for-the-badge&logo=Consul&logoColor=white)
![Vault](https://img.shields.io/badge/Vault-FFEC6E.svg?style=for-the-badge&logo=Vault&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED.svg?style=for-the-badge&logo=Docker&logoColor=white)
![Tomcat](https://img.shields.io/badge/Apache%20Tomcat-F8DC75.svg?style=for-the-badge&logo=Apache-Tomcat&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032.svg?style=for-the-badge&logo=Git&logoColor=white)
![Github](https://img.shields.io/badge/GitHub-181717.svg?style=for-the-badge&logo=GitHub&logoColor=white)


```

* Spring Cloud
* H2DataBase
* Docker Compose
* Keycloak

```

## Installation
1. Clone this repo
```
git clon <!--links of repo-->
```
2. Install all the dependencies
```
npm install
```
4. run all services (after install maven dependencies in intellijIDE)
5. run front project
```
ng serve
```
## Run Project From Docker 
```
To Run This Project With Docker You should to have docker engine in your machine and just trying
to use docker compose file with this command:
1. You should to be inside of this project in your machine (change direcotory to docker compose file directory)
  $ cd directoryFile
2. run docker compose
  $ docker compose up -d --build
```
## Project Dependencies
<table>
    <tr>
        <th>Reservation</th>
        <th>Resource</th>
        <th>Gateway</th>
        <th>Configuraion</th>
    </tr>
    <tr>
        <td><a href="https://github.com/Elma-dev/Build_Decorize_MS_Architect/blob/main/reservation-service/pom.xml"><img src="https://upload.wikimedia.org/wikipedia/commons/5/52/Apache_Maven_logo.svg"/></a></td>
        <td><a href="https://github.com/Elma-dev/Build_Decorize_MS_Architect/blob/main/ressource_service/pom.xml"><img src="https://upload.wikimedia.org/wikipedia/commons/5/52/Apache_Maven_logo.svg"/></a></td>
        <td><a href="https://github.com/Elma-dev/ManageViolation_APP_Spring_MS/blob/3f7db6a29bbc6196781d8276c4fa50a8dbdcdfe1/Infractin_MS/pom.xml"><img src="https://upload.wikimedia.org/wikipedia/commons/5/52/Apache_Maven_logo.svg"/></a></td>
        <td><a href="https://github.com/Elma-dev/Build_Decorize_MS_Architect/blob/main/configuration_service/pom.xml"><img src="https://upload.wikimedia.org/wikipedia/commons/5/52/Apache_Maven_logo.svg"/></a></td>
</table>

## Vault & Consul Installation
![image](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/bfd9db00-c0a3-4701-b43f-9cb99178d011)
### Consul
```
The utility of Consul extends beyond mere service discovery; it encompasses various facets of distributed systems
management,such as health checking, key-value storage, and distributed locking.
```
* Installation Of **Consul**:
```
brew install consul
```
* Run **Consul** in dev mode:
```
consul agent -dev
```
* Join **Consul** Ui:
```
http://localhost:8500
```
* Use Consul with Micro Services as a Discovery:
  1. you should to add ```consul discovery```dipendency.
  2. add ```@EnableConsulDiscovry``` to the main of any ms.
### Vault
```
In the realm of distributed systems and cloud-native applications, the management of sensitive information—such as
API keys, passwords, and encryption keys—is a critical concern. Vault addresses this challenge by offering a centralized
platform for storing, managing, and accessing secrets securely.
```
* Installation Of **Vault**:
```
brew install vault
```
* Run **Vault** in dev mode:
```
Vault server -dev
```
* Join **Vault** Ui:
```
http://localhost:8200
```
* To use vault in your application you should to add this params
```
spring.config.import=optional:consul:,vault:
spring.cloud.vault.token=yourToken
spring.cloud.vault.scheme=http
spring.cloud.vault.kv.enabled=true
```
## Keycloak
```
Keycloak is an open-source identity and access management (IAM) solution developed by Red Hat. It provides a
comprehensive set of capabilities for managing user identities, enforcing authentication and authorization policies,
and securing applications and services. 
```
1. Download Kycloak From Keycloak Website (binary version)
2. in keyclaok folder you can run keycloak with this command:
  ```
  bin/kc.sh start-dev
  ```
3. join keycloak ui
   ```
   http://localhost:8080
   ```
4. create Application Realm/Clients/Users/Roles from keycloak ui
   ![‎Keycloak ‎002](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/fe9da4e1-b900-4700-817d-a0849d4c0fce)
   ![‎Keycloak ‎001](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/e9087643-2e7f-4039-8ead-9391f17588f5)
   ![‎Keycloak ‎003](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/ceec0b5e-1818-4040-b15d-d7374ae144d5)
   ![‎Keycloak ‎004](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/c72baf22-8ff1-4cfe-a27e-a94b1f916560)
   ![‎Keycloak ‎005](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/91208971-0061-4aa6-8f32-8266e51464dc)
# Project: Micro serrvice Architect & Diagram Class
## Micro serrvice Architect
  
  This Project has two microservices:
  
    - resources-service: this allowed the user to control the resources he may reserve from other services as a client. 
    - reservation-service: with this service, the user may manage clients and reservations in addition to making new
    reservations for new people.
    
  Every service has: 
  
    - Its own database; 
    - User-friendly interfaces that facilitate ease of use.

  ![image](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/d5565b0c-43b1-4d54-9b9f-27885f7765db)
## Diagram Class
![Screen Shot 2023-12-31 at 01 24 54](https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/e48f5c63-28d8-40b5-b67c-5100611db25e)

# Services Tree
## Configuration Service
```
├── dockerfile
├── mvnw
├── mvnw.cmd
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── dev
    │   │       └── elma
    │   │           └── configuration_service
    │   │               └── ConfigurationServiceApplication.java
    │   └── resources
    │       └── application.properties
```
## Gateway service
```
.
├── dockerfile
├── mvnw
├── mvnw.cmd
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── dev
    │   │       └── elma
    │   │           └── gateway_service
    │   │               └── GatewayServiceApplication.java
    │   └── resources
    │       └── application.properties
```

## Resource service
```
.
├── Dockerfile
├── mvnw
├── mvnw.cmd
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── dev
    │   │       └── elma
    │   │           └── ressource_service
    │   │               ├── Dtos
    │   │               │   └── ResourceClient.java
    │   │               ├── Mappers
    │   │               │   └── ResourceMappers.java
    │   │               ├── Repositories
    │   │               │   └── ResourceRepo.java
    │   │               ├── ResourceServiceApplication.java
    │   │               ├── entities
    │   │               │   └── Resource.java
    │   │               ├── enums
    │   │               │   └── ResourceType.java
    │   │               ├── security
    │   │               │   └── SecurityConfig.java
    │   │               └── web
    │   │                   └── ResourceRestController.java
    │   └── resources
    │       └── application.properties
```
## Reservation service
```
.
├── Dockerfile
├── mvnw
├── mvnw.cmd
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── dev
    │   │       └── elma
    │   │           └── reservationservice
    │   │               ├── Dtos
    │   │               │   ├── PersonClient.java
    │   │               │   └── ReservationClient.java
    │   │               ├── ReservationServiceApplication.java
    │   │               ├── entities
    │   │               │   ├── Person.java
    │   │               │   └── Reservation.java
    │   │               ├── feign
    │   │               │   └── ResourceClient.java
    │   │               ├── mappers
    │   │               │   └── ReservationMapper.java
    │   │               ├── models
    │   │               │   └── Resource.java
    │   │               ├── repositories
    │   │               │   ├── PersonRepo.java
    │   │               │   └── ReservationRepo.java
    │   │               ├── security
    │   │               │   ├── FeignAdapter.java
    │   │               │   └── SecurityConfig.java
    │   │               └── web
    │   │                   ├── PersonRestController.java
    │   │                   └── ReservationRestController.java
    │   └── resources
    │       └── application.properties
```
# Problems: Solutions
1. gateway cors
   ```yaml
   spring:
    cloud:
      gateway:
        globalcors:
          corsConfigurations:
            '[/**]':
              allowedOrigins: "*"
              allowedHeaders: "*"
              allowedMethods:
                - GET
                - POST
                - PUT
                - DELETE
                - OPTION
   
   ```
3. server spring security cors
   ```java
   @Bean
    CorsConfigurationSource corsConfigurationSource() {
    	CorsConfiguration configuration = new CorsConfiguration();
    	configuration.setAllowedOrigins(Arrays.asList("https://example.com"));
    	configuration.setAllowedMethods(Arrays.asList("GET","POST"));
    	UrlBasedCorsConfigurationSource source = 
    				new UrlBasedCorsConfigurationSource();
    	source.registerCorsConfiguration("/**", configuration);
    	return source;
    }
   ```
5. open feign adapter
   ```java
     @Component
      public class FeignInterceptor implements RequestInterceptor {
          @Override
          public void apply(RequestTemplate requestTemplate) {
              SecurityContext context = SecurityContextHolder.getContext();
              JwtAuthenticationToken authentication = 
      					(JwtAuthenticationToken) context.getAuthentication();
              String tokenValue = authentication.getToken().getTokenValue();
              requestTemplate.header("Authorization","Bearer "+tokenValue);
          }
      }
   ```

# Web Services Test
<table align="center">
    <tr>
        <th>Consul</th>
        <th>Keycloak</th>
    </tr>
    <tr>
        <td><img src="https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/c875291e-d238-43b0-9f33-af3e1fb6e641"/></td>
        <td><img src="https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/bc0c3189-598b-46e0-82bc-17fb69f6f88c"/></td>
    </tr>
</table>

<table align="center">
    <tr>
        <th>Security Test: Get Token</th>
        <th>Token Decoder </th>
        <th>Test Token</th>
    </tr>
    <tr>
        <td><img src="https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/8f5f024b-c467-43c6-9c4c-add9b20d5e9a)https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/8f5f024b-c467-43c6-9c4c-add9b20d5e9a"/></td>
        <td><img src="https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/5220a41f-cb1e-4e0a-8791-86f0a3ed4cea"/></td>
        <td><img src="https://github.com/Elma-dev/build_decorize_secured_full_ms_architect_front_back_angular_spring_boot/assets/67378945/be7dded9-c432-411e-81dd-8730e289fa41"/></td>
    </tr>
</table>
