# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
~~~
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
~~~
## PROGRAM
CLIENT
~~~
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
~~~
SERVER
~~~
SERVER: 
 
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
     ClientMessage=c.recv(1024).decode()
     print("Client > ",ClientMessage) 
     msg=input("Server > ") 
     c.send(msg.encode())
~~~
## OUTPUT
CLIENT
![image](https://github.com/sharmitha3/3b_CHAT_USING_TCP_SOCKETS/assets/145974496/ff76e938-f5d1-4c85-a319-1f3f9485d0a1)
SERVER
![image](https://github.com/sharmitha3/3b_CHAT_USING_TCP_SOCKETS/assets/145974496/4212a6ca-1773-4472-b910-87e91f8357ab)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
