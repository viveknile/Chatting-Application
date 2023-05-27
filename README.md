# Chat Application using Java Socket Programming

This is a simple chat application implemented using Java Socket Programming. The application allows multiple clients to connect to a server and communicate with each other by sending messages.

## Prerequisites

- Java Development Kit (JDK) installed on your system.
- Basic knowledge of Java programming language and socket programming concepts.

## How to Run the Application

1. Clone the repository or download the source code to your local machine.

2. Open the terminal (Command Prompt) and navigate to the project directory.

3. Compile the Java source files using the following command:

   ```shell
   javac Server.java
   javac Client.java
   ```

4. Start the server by running the following command:

   ```shell
   java Server
   ```

5. Start multiple client instances by running the following command:

   ```shell
   java Client
   ```

6. The clients will prompt you to enter the IP address and port number of the server. Enter the appropriate values to connect to the server.

7. Once the clients are connected to the server, you can start sending messages. Any message sent by a client will be broadcasted to all other connected clients.

## File Structure

The project directory contains the following files:

- `Server.java`: This file implements the server side of the chat application. It creates a server socket, accepts client connections, and handles communication between clients.

- `Client.java`: This file implements the client side of the chat application. It connects to the server using a socket and allows the user to send and receive messages.

## How it Works

The chat application works based on a client-server model. The server listens for client connections on a specific port. Once a client is connected, the server creates a separate thread to handle communication with that client.

The clients connect to the server by specifying the server's IP address and port number. Upon successful connection, the clients can send messages to the server, which will broadcast those messages to all other connected clients.

The communication between the server and clients is established using sockets. The server and clients use `Socket` and `ServerSocket` classes from the `java.net` package to create and manage the sockets.

The server uses a list of connected clients to keep track of the active connections. When a client sends a message, the server iterates over the list and sends the message to each connected client except the one who sent the message.

## Customize and Extend

Feel free to modify and extend the chat application according to your needs. Here are some possible improvements or features you can add:

- Implement username functionality: Allow clients to choose a username when they connect and display the usernames with the messages.
- Implement private messaging: Allow clients to send messages to specific clients instead of broadcasting to all clients.
- Add authentication: Implement a login system to authenticate clients before allowing them to connect.
- Implement encryption: Secure the communication between the server and clients by adding encryption mechanisms.

## Resources

- [Java Socket Programming Tutorial](https://docs.oracle.com/javase/tutorial/networking/sockets/index.html): Official Oracle documentation on Java Socket Programming.
- [Socket (Java Platform SE 16)](https://docs.oracle.com/en/java/javase/16/docs/api/java.base/java/net/Socket.html): Java API documentation for the Socket class.
- [ServerSocket (Java Platform SE 16)](https://docs.oracle.com/en/java/javase/16/docs/api/java.base/java/net/ServerSocket.html): Java API documentation for the ServerSocket class.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

The initial version of this chat application was inspired by a tutorial on Java Socket Programming by [Cave of Programming](https://www.caveofprogramming
