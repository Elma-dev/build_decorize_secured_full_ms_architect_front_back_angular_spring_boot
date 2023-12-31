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
Installation Of Consul:
```
brew install consul
```
Run Consul in dev mode:
```
consul agent -dev
```
Join Consul Ui:
```
http://localhost:8500
```
Use Consul with Micro Services as a Discovery:
  1. you should to add ```consul discovery```dipendency.
  2. add ```@EnableConsulDiscovry``` to the main of any ms.
### Vault
```
In the realm of distributed systems and cloud-native applications, the management of sensitive information—such as
API keys, passwords, and encryption keys—is a critical concern. Vault addresses this challenge by offering a centralized
platform for storing, managing, and accessing secrets securely.
```
