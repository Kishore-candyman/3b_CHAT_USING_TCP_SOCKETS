# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',9000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

SERVER:

```
import socket
s=socket.socket()
s.bind(('localhost',9000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```

## OUPUT
CLIENT:

![image](https://github.com/user-attachments/assets/56a0b767-5d9b-4900-87c6-7546a4a2b2cb)

SERVER:

![image](https://github.com/user-attachments/assets/8a7f0315-58ed-4c13-8a80-78b9b097abfe)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
