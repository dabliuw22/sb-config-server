# Config Server

Servidor de configuración para microservicios.

1. Dependencias:
	* Cloud Config: Config Server
	* Actuator

2. Anotar con *@EnableConfigServer* la clase de configuración.

3. Renombrar *application.yml* por *bootstrap.yml* y agregar:
```[yml]
server:
  port: 8989
spring:
  application:
    name: config-server
  cloud:
    config:
      server:
        git:
          uri: file:/home/user/Documentos/sb-config-server-repo
```