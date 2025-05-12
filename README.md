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
## PROGRAM
client:

import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

msg=input("Client > ")

s.send(msg.encode())

print("Server > ",s.recv(1024).decode())

server:

import socket

s=socket.socket()

s.bind(('localhost',8000))

s.listen(5)

c,addr=s.accept()

while True:

ClientMessage=c.recv(1024).decode()

c.send(ClientMessage.encode())


## OUPUT

CLIENT:

![image](https://github.com/user-attachments/assets/405a25ee-4cf6-4d18-94e2-edd68cf63d5f)

SERVER:

![image](https://github.com/user-attachments/assets/a6663aca-5624-4b04-b8d8-98b760764313)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
