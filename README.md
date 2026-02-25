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
## server.py
```
import socket
s=socket.socket()
s.bind(('127.0.0.1',12345))
s.listen(5)
print("server is listening..")
c,addr=s.accept()
while True:
    Message=c.recv(1024).decode()
    print("Client:",Message)
    msg=input("Server:")
    c.send(msg.encode())
c.close()
```

## client.py
```
import socket
s=socket.socket()
s.connect(('127.0.0.1',12345))
print("connected successfully!!")
while True:
    msg=input("Client:")
    s.send(msg.encode())
    print("Server:",s.recv(1024).decode())
```

## OUPUT
<img width="1002" height="350" alt="image" src="https://github.com/user-attachments/assets/6a30f9c1-4e46-4a61-8403-4b64ee1fda3d" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
