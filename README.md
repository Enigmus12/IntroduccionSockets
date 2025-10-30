# IntroduccionSockets

Aplicación básica de WebSockets usando Spring Boot que demuestra comunicación en tiempo real entre servidor y cliente.

## Descripción

Este proyecto implementa un servidor WebSocket que envía mensajes de tiempo cada 5 segundos a todos los clientes conectados. Utiliza Spring Boot con WebSocket y un endpoint temporal para broadcasting de mensajes.

## Tecnologías

- Java
- Spring Boot 2.3.1
- WebSockets (javax.websocket)
- Maven

## Estructura del Proyecto

- `WSStartApp.java` - Clase principal de Spring Boot
- `TimerEndpoint.java` - Endpoint WebSocket que maneja las conexiones
- `TimedMessageBroker.java` - Componente que envía mensajes programados cada 5 segundos
- `WSConfigurator.java` - Configuración de WebSocket
- `index.html` - Cliente web para conectarse al WebSocket

## Requisitos

- Java 8 o superior
- Maven 3.x

## Instalación y Ejecución

1. Clonar el repositorio:
```bash
git clone https://github.com/Enigmus12/IntroduccionSockets.git
cd IntroduccionSockets/Sockets
```

2. Compilar el proyecto:
```bash
mvn clean install
```

3. Ejecutar la aplicación:
```bash
mvn spring-boot:run
```

4. Abrir el navegador en `http://localhost:8080`

## Uso

Una vez iniciada la aplicación, abre `http://localhost:8080` en tu navegador. La página se conectará automáticamente al WebSocket y comenzará a recibir mensajes con la hora actual cada 5 segundos.

## Endpoint WebSocket

- **URL**: `ws://localhost:8080/timer`
- **Frecuencia de mensajes**: cada 5 segundos

## Autor

Enigmus12