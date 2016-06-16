# TaxiPak Client Interface Specification - PI

## Preface


## Communication Media


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

