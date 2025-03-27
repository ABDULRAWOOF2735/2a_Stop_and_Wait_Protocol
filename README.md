# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
Developed by: ABDULRAWOOF
REG NO: 212224230003
### Client
~~~
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
~~~
### Server
~~~
import socket
 s=socket.socket()
 s.connect(('localhost',8000))
 while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
~~~
## OUTPUT
## Client

![WhatsApp Image 2025-03-27 at 11 29 03_e7a004 client](https://github.com/user-attachments/assets/e5973c18-0bdd-4e02-8b5d-865b663c7a8b)

## Server

![WhatsApp Image 2025-03-27 at 11 29 03_0cd1eae9](https://github.com/user-attachments/assets/87d61186-9541-4688-833a-e111c04e38ca)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
