# TaxiPak Client Interface Specification - PI

## Preface
This document describes the functionality of the application PI for use with TaxiPak. The application has been developed by MobileSoft Consulting, Inc. It is designed to be an application that converts/takes care of the communicated information from an external client application. The process communicating with the PI is referred to as the external process (EXTP).

## Communication Media
The PI has been built so it is possible to have more than one communication link. In fact, the limitation on the number of simultaneously running links is only limited by the operating system and machine resources.  For the communication PI is using network communication sockets.

### Sockets Used in PI
Sockets have been used to take care of the communication of message between PI and EXTP’s. It is a clietn- server based model with a concurrent server. It is possible to have an unlimited number of EXTP’s connecting to the PI server.  
### Setup of the Socket
|Parameter | Value    |
|----------|:--------:|
| PROTOCOL | IP |
| TYPE | SOCK_STREAM|
| ADDRESS_FAMILY| AF_INET|
| LOCAL_ADDRESS | INADDR_ANY |
| PORT | PI_PORT |
  
> A simple transfer of sequential blocks of data is needed done with the usual read/write functions. The use of TCP/IP sockets will buffer data for the bi-directional communication and provide sequenced, reliable transmission of data.
### Setup of the Port
| Port | Number |
|------|:------:|
| PI_PORT| 3000|


