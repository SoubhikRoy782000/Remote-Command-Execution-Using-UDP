# Remote-Command-Execution-Using-UDP

Aim –

Remote command server using TCP and UDP as transport protocol. Clients interact with the server sending some specific commands and the server holds that process, and sends back to client an response. 
the server logs all the commands that were sent by the client.

Given Requirements –

There are two hosts, Client and Server. The Client sends a command to the Server, which executes the command and sends the result back to the Client.

Algorithm -

Server:

Step 1: Include the necessary header files.
Step 2: Create a socket using socket function with family AF_INET, type as SOCK_DGRAM.44
Step 3: Initialize server address to 0 using the bzero function.
Step 4: Assign the sin_family to AF_INET, sin_addr to INADDR_ANY, sin_port to dynamically 
assigned port number.
Step 5: Bind the local host using the bind() system call.
Step 6: Within an infinite loop, receive the command to be executed from the client.
Step 7: Append text “> temp.txt” to the command.
Step 8: Execute the command using the “system()” system call.
Step 9: Send the result of execution to the Client using a file buffer.

Client:

Step 1: Include the necessary header files.
Step 2: Create a socket using socket function with family AF_INET, type as SOCK_DGRAM.
Step 3: Initialize server address to 0 using the bzero function.
Step 4: Assign the sin_family to AF_INET.
Step 5: Get the server IP address and the Port number from the console.
Step 6: Using gethostbyname() function assign it to a hostent structure, and assign it to sin_addr of the 
server address structure.
Step 7: Obtain the command to be executed in the server from the user.
Step 8: Send the command to the server.
Step 9: Receive the output from the server and print it on the console.
