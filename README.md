# Stop-and-wait-protocol

IMPLEMENTATION OF STOP AND WAIT PROTOCOL

EXP: 1(a)

DATE:

AIM:

To write a python program to perform stop and wait protocol

ALGORITHM:

1. Start the program.

2. Get the frame size from the user

3. To create the frame based on the user request.

4. To send frames to server from the client side.

5. If your frames reach the server it will send ACK signal to client

otherwise it will sendNACK signal to client.

6. Stop the program

PROGRAM:

CLIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
```
SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
REG NO:212222040093

OUTPUT:

CLIENT:
![image](https://github.com/MaheshMuthuL/Stop-and-wait-protocol/assets/135570619/97876e03-ea09-4351-8634-2c0f9ad1b3a2)

SERVER:
![image](https://github.com/MaheshMuthuL/Stop-and-wait-protocol/assets/135570619/356cadfb-d27f-4945-abe3-8bfa02ee6c9e)

RESULT:

Thus, python program to perform stop and wait protocol was successfully executed.
