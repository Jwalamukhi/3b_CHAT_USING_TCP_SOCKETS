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
DEVELOPED BY:JWALAMUKHI S
REGISTER:212223040079

CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
   msg=input("CLIENT > ")
   s.send(msg.encode())
   print("CLIENT > ",s.recv(1024).decode())
```

SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
     ClientMessage=c.recv(1024).decode()
     print("CLIENT > ",ClientMessage)
     msg=input("SERVER > ")
     c.send(msg.encode()) 
```
## OUTPUT

CLIENT

![image](https://github.com/user-attachments/assets/2c8f651d-1f55-46dd-a1de-7db1d3412d3a)



SERVER

![image](https://github.com/user-attachments/assets/9d082cc9-888b-47c0-b8d2-5f471bb9a941)

  
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
