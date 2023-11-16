
# Chat Application in Python

This document provides an overview of the key functions, methods, and classes used in the Python chat application project. It includes examples to illustrate their usage.

## Server-Side

### Key Functions and Methods

#### Socket Creation
- `socket.socket(socket.AF_INET, socket.SOCK_STREAM)`
  - Creates a new socket using IPv4 and TCP.
  - Example: `server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)`

#### Binding and Listening
- `server.bind((HOST, PORT))`
  - Binds the server to a specific IP and port.
  - Example: `server.bind(('127.0.0.1', 65432))`
- `server.listen()`
  - Configures the server to accept connections.
  - Example: `server.listen()`

#### Accepting Connections
- `client, address = server.accept()`
  - Accepts a connection from a client.
  - Example: `client, address = server.accept()`

#### Handling Clients
- `def handle_client(client):`
  - A function to manage communication with a connected client.
  - Example:
    ```python
    def handle_client(client):
        # Code to handle client communication
    ```

### Threading
- `threading.Thread(target=handle_client, args=(client,))`
  - Creates a new thread to handle each client.
  - Example: `client_thread = threading.Thread(target=handle_client, args=(client,))`

## Client-Side

### Key Functions and Methods

#### Connecting to Server
- `client.connect((host, port))`
  - Connects the client to the server at the given host and port.
  - Example: `client.connect(('127.0.0.1', 65432))`

#### Sending and Receiving Messages
- `client.send(message.encode('utf-8'))`
  - Sends an encoded message to the server.
  - Example: `client.send('Hello Server!'.encode('utf-8'))`
- `message = client.recv(1024).decode('utf-8')`
  - Receives a message from the server and decodes it.
  - Example: `message = client.recv(1024).decode('utf-8')`

### Threading for Receiving Messages
- `threading.Thread(target=receive)`
  - Creates a new thread for receiving messages from the server.
  - Example: `receive_thread = threading.Thread(target=receive)`

