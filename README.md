# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
SERVER
## PROGRAM:
```
import socket

server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

host = '127.0.0.1'
port = 5000

server_socket.bind((host, port))

server_socket.listen(1)
print("Server is waiting for connection...")

conn, addr = server_socket.accept()
print("Connected with:", addr)

data = conn.recv(1024).decode()
print("Received from client:", data)

conn.send(data.encode())

conn.close()
server_socket.close()
CLIENT

import socket

client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

host = '127.0.0.1'
port = 5000

client_socket.connect((host, port))

message = input("Enter message: ")
client_socket.send(message.encode())

data = client_socket.recv(1024).decode()
print("Echo from server:", data)

client_socket.close()
```
## OUTPUT
<img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/59b4848f-caa0-48a1-b75f-e438b8869b9c" />

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/5f03d756-1d5a-4a90-b53b-cee558d28939" />



## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.


Footer
