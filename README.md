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
### CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

```
### SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8080))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())

```
## OUTPUT
### CLIENT:
![Screenshot 2024-04-29 141309](https://github.com/Ratheesh28/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/138849186/6b08d6cf-14bd-47e5-a1e0-745b473fd154)

### SERVER:
![Screenshot 2024-04-29 141342](https://github.com/Ratheesh28/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/138849186/2a8ca2b4-e2a3-4bf4-9aa5-47490373ff68)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
