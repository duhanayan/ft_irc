<h1 align="center"> 📮 IRC SERVER </h1>

## 🤔 About
This project is about creating our own IRC server. We used an actual IRC client to connect to our server and test it.
**IRC** (Internet Relay Chat) is a protocol for real-time text messaging between internet-connected computers created in **1988**. It is mainly used for group discussion in chat rooms called “**channels**” although it supports private messages between two users, data transfer, and various client-side commands.

#### Skills

- Network & system administration
- Rigor
- Object-oriented programming

### Mandatory part
  - We have to develop an IRC server in C++ 98.
  - The server must be capable of handling multiple clients at the same time and never hang.
  - Only 1 poll() (or equivalent) can be used for handling all these operations (read, write, but also listen, and so forth).
  - An IRC client must be able to connect to your server without encountering any error.
  - Communication between client and server has to be done via TCP/IP (v4).
  - Using the IRC client with our server must be similar to using it with any official IRC server. However, we only have to implement the following features:
    -  We must be able to authenticate, set a nickname, a username, join a channel, send and receive private messages using the IRC client.
    -  All the messages sent from one client to a channel have to be forwarded to every other client that joined the channel.
    -  We must have operators and regular users.
    -  Then, we have to implement the commands that are specific to operators.

## 🔑 Our IRC Commands
These are the available commands in our IRC Server:
  - **PASS**: The **PASS** command is used to set a 'connection password'.
  - **NICK**: **NICK** command is used to give user a nickname or change the existing one.
  - **USER**: The **USER** command is used at the beginning of connection to specify the username, hostname and realname of a new user.
  - **QUIT**: A client session is terminated with a quit message.
  - **JOIN**: The **JOIN** command is used by a user to request to start listening to the specific channel.
  - **PART**: The **PART** command causes the user sending the message to be removed from the list of active members for all given channels listed in the parameter string.
  - **KICK**: The **KICK** command can be used to request the forced removal of a user from a channel.
  - **PRIVMSG**: **PRIVMSG** is used to send private messages between users, as well as to send messages to channels.
  - **NOTICE**: The **NOTICE** command is used for Operators to make announce.
  - **WHO**: The **WHO** command is used for list members for specified channel.
  - **LIST**: The **LIST** command is used for list channels.
  - **MEMBER**: The **MEMBER** command is used for list channels you are member of.

## ⚙️ Start IRC Server
To compile the program, use:
  - `make`
To start the Server, use:
  - `./ircserv <port> <password>`
    - **port**: The port number on which your IRC server will be listening to for incoming IRC connections.
    - **password**: The connection password. It will be needed by any IRC client that tries to connect to your server.
To connect to the server, you can use:
  - `nc <IP ADDRESS> <PORT>`
    - **IP ADDRESS**: Host IP address.
    - **PORT**: The PORT that the server listening on.
  - You can also use an IRC Client e.g LimeChat, WeeChat...
