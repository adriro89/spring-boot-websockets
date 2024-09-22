# Spring Boot and Websockets Chat Application

This application is a simple chat service based on WebSocket, built with Spring Boot. It includes a very basic and user-friendly interface that allows users to interact with the backend and WebSocket seamlessly. Users can send and receive messages in real-time through a WebSocket connection.

## Technologies Used

- Java 17
- Spring Boot
- WebSocket
- STOMP (Simple Text Oriented Messaging Protocol)
- Lombok

## Project Structure

The project is organized into three packages:

- **config**: This package contains the WebSocket configuration.
  - **WebSocketConfig.java**: Configures the WebSocket server, defines STOMP endpoints, and enables the message broker.
  - **WebSocketEventListener.java**: Listens for WebSocket disconnection events and sends a leave message to the public channel.


- **controller**: This package contains the controllers that handle messages sent by users.
  - **ChatController.java**: Manages chat messages and user additions. Messages are sent to the public channel for all connected users to receive.


- **model**: This package defines the model classes used in the application.
  - **ChatMessage.java**: Represents a chat message, including content, sender, and message type.
  - **MessageType.java**: Enum that defines message types (CHAT, JOIN, LEAVE).

In addition to these packages, you can find the HTML file along with its CSS and JavaScript in the `resources` directory.

## Running the project

The application runs on port `8080`. To start the application use the following command:

```bash
   ./mvnw spring-boot:run
   ```

Once the application is running, you can open multiple browser tabs to create multiple users and send messages that every user will receive in real-time.

## Acknowledgments
This code has been uploaded following a tutorial from [Ali Bouali's](https://github.com/ali-bouali).

Tutorial link: https://www.youtube.com/watch?v=TywlS9iAZCM