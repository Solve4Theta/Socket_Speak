# Socket_Speak
First time exploring the socket interface provided for the C programming language.
There is an option for the client to be an intermediary server in hopes to lighten the load on the server as the original aim was to run the server on an old Raspberry Pi. This will be prompted by the client program. 
The project was developed on Linux, so it should be compiled and run on Linux.

Dependencies & Usage:
For compilation the openssl and pthread libraries are required.
To install openssl - sudo apt install libssl-dev.
To install pthread on Ubuntu based systems - sudo apt install libpthread-stubs0-dev.
To compile the server program - gcc -o main *.c -lssl -lcrypto -lpthread.
To run the server program - ./main.
To compile the client program - gcc -o main *.c -lssl -lcrypto -lpthread.
To use the client program - ./main <host_ip> <portnum>.
Make sure the server is running before you connect through the client.

The project is far from perfect. Memory leaks are abundant, especially on the server side and there is a problem with the openssl library once the intermediary server receives a certain amount of client messages.
Nonetheless, it has been interesting and informative working with sockets and encryption in C and the shortcomings of this project are a reason to revisit it in the future. 
