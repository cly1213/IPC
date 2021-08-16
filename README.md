# IPC (Inter Process Communication)
- UNIX Domain Socket
- TCP/IP Socket

## UNIX socket
A UNIX socket is an inter-process communication mechanism that allows bidirectional data exchange between processes running on the same machine.

## IP sockets
IP sockets (especially TCP/IP sockets) are a mechanism allowing communication between processes over the network. 
In some cases, you can use TCP/IP sockets to talk with processes running on the same computer (by using the loopback interface).

### IP(Internet Protocol)
- unreliable
- best-effort delivery
- connectionless

#### TCP(Transport Control Protocol)
- reliable
- connection-oriented

#### UDP(User Datagram Protocol)
- unreliable
- connectionless


UNIX domain sockets know that they’re executing on the same system, so they can avoid some checks and operations (like routing); 
which makes them faster and lighter than IP sockets. 
So if you plan to communicate with processes on the same host, this is a better option than IP sockets.


Ref:

https://serverfault.com/questions/124517/what-is-the-difference-between-unix-sockets-and-tcp-ip-sockets

https://stackoverflow.com/questions/14973942/tcp-loopback-connection-vs-unix-domain-socket-performance
