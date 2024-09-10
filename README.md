# Echoserver

Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

## echo-client.py:
```
import socket

s=socket.socket()

s.connect(('localhost',65124))

while(1):

  msg=input("Client>")

  s.send(msg.encode())

  print("Server>"+s.recv(1024).decode())

```

## echo-server.py:
```

import socket

s=socket.socket()

s.bind(('localhost',65124))

s.listen(5)

c,addr=s.accept()

while(1):

   msg=c.recv(1024).decode()

   print(msg)

   c.send(msg.encode())

```
## OUTPUT:

![ethn exp1](https://github.com/user-attachments/assets/64ab8f14-c282-476b-85e9-d82c41d94cb6)

## RESULT:

The program is executed successfully.
