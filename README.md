# TCP-Chat-Application-in-Java

# TCP Chat Application in Java

## Project Overview

This project is a simple TCP-based chat application implemented in Java. It consists of a server and multiple clients that can connect to the server to exchange messages. The application demonstrates basic concepts of networking, multithreading, and socket programming in Java.

## Features

- Multiple clients can connect to the server and communicate with each other.
- Each client can set a username upon connection.
- Clients can change their username using the `/user` command.
- Clients can disconnect from the chat using the `/quit` command.
- Messages from clients are broadcasted to all connected clients.

## Key Concepts Used

- **Socket Programming:** Utilizes Java's `Socket` and `ServerSocket` classes to handle client-server communication.
- **Multithreading:** The server handles multiple clients concurrently using `ExecutorService` for thread management.
- **I/O Streams:** Uses `BufferedReader` and `PrintWriter` for reading from and writing to sockets.
- **ExecutorService:** `Executors.newCachedThreadPool()` is used to manage a pool of threads for handling multiple client connections.
- **Synchronization:** Proper handling of shared resources (like the list of connected clients) to ensure thread safety.

## My Learnings

- **Networking Basics:** Understanding how TCP/IP works and establishing a connection between a client and a server.
- **Concurrency in Java:** Implementing a multithreaded server to handle multiple clients simultaneously.
- **Exception Handling:** Managing I/O exceptions and ensuring the server and client can handle unexpected disconnections gracefully.
- **Command Handling:** Parsing and executing commands from clients, such as changing usernames or quitting the chat.
- **Resource Management:** Ensuring proper closing of sockets and streams to prevent resource leaks.

## How to Run

### Server

Compile and run the `Server.java` file:
```sh
javac Server.java
java Server
```

### Client

Compile and run the `Client.java` file:
```sh
javac Client.java
java Client
```

## Usage

- When the client connects to the server, it will be prompted to enter a username.
- To change the username, type `/user new_username`.
- To quit the chat, type `/quit`.

## Future Enhancements

- **Improved User Input Validation:** Ensure usernames are unique and valid, and sanitize all inputs to prevent malicious commands.
- **Enhanced User Interface:** Develop a graphical user interface (GUI) for a more user-friendly experience.
- **Private Messaging:** Add functionality for clients to send private messages to specific users.
- **Persistence:** Implement a database to store chat history and user information.

## Acknowledgments

Inspired by basic chat applications and tutorials on socket programming in Java.
