# Socket_Learning_TCP_Client
# 5/27/2021
Create TCP socket communication client.

## Sample project files
---
### Socket_Learning_TCP_Client(.h and .cpp)
---
We need take following steps to create socket client for TCP communication:
1. Start up socket with function WSAStartup() to find the usable Windowsock DLL. We use Winsock 2.2 dll in this sample as the sample in MSDN.
2. Create socket client with the socket constructor. Parameter SOCK_STREAM was used for TCP protocol.
3. Transfer the server ip adress from string to in_addr.
4. Bind the socket server created in Step.2 with the address. AF_INET was the family used for TCP protocol. Port number also needed to be specific in this step.
5. Connect the client to the sever with connect() function.
6. If the connection established correctly, then send message to the sever with send() function.
7. WSACleanup was used to clean all the information and finished the use of Winsock dll.
 
