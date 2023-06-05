# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE :27-04-2023

## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.


## ALGORITHM :
### STEP 1: Import the necessary modules in python
### STEP 2: Create a socket connection to using the socket module.
### STEP 3: Send message to the client and receive the message from the client using the 
  Socket module in server.
### STEP 4: Send and receive the message using the send function in socket.


## PROGRAM :
### Developed by: Kalpana S
### Register No: 212222040069
## Client :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server :
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
 ```

## OUTPUT :
### CLIENT OUTPUT :
![ex08 client output](https://github.com/Kalpanareshma/EX-8/assets/122040453/2f26f09b-aaa4-47e8-af76-95651b760ea4)
### SERVER OUTPUT :
![ex08 server output](https://github.com/Kalpanareshma/EX-8/assets/122040453/81010722-f2ba-4bdb-9b78-8a2be5e84951)

## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
