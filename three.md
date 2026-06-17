OSI-model
purpose of networking:
allow two hosts to share data with one another 

host must follow a set of rules:
example-english language has rules
spanish has its own rules

like the same way networking are devided into seven layers which is called OSI model 
-each layer serves a specific function
-if all layers are functioning hosts can share data 

Layer 1: Physical layer
-transporting bits 
-computer data exits in the form of bits(1,0)
-something has to transport those bits between hosts
-L1 technologies: Cables
twisted pair ethernet 
coaxial,fiber,wifi,repeaters,hubs

layer 2: data link 
-interact with the wire(ie physical layer)
NIC network interface cards/wifi access cards
-HOP to HOP
adressing scheme - MAC adresses
these are 48 bits represented as 12 hex digits 
93-65-9c-3b-8A-e5(windows) / 93:65:9c:3b:8A:e5(linux) / 9465.963b.8ae5(cisco,routers,switches)
every single NIC has a unique MAC adresses
L2 technologies: NIC,switches
often communication between hosts require multiple hops 

Layer 3 : NETWORK
-end to end
adressing scheme - IP adresses
32 bits represented as 4 octets each 0-255
L3 technologies- routers,hosts,anythign with ip
questions:
if mac adresses exits why we need ip adresses?
answer:
c1 has an ip adress and c3 has an ip adress between them tehre are multiple routers becuase its a distacne communication so 
IP- states the end to end connection the file transfer will have source as c1 and destination as c3 
MAC- state the hop to hop now the transfer of data to one router to another router information will be avialable to this MAC adress so it can perform hop to hop according to reach the final destination IP adresses

ARP-Adress resolution protocal
links a L3 adress to L2 adress


Layer 4 : Transport 
-service to service
distinguish data streams 
Adressing scheme - ports 
0-65535 - TCP-favours reliability
0-65535 - UDP-favours efficiency
-servers listen for requests to predefined ports 
-client selcts a rondom port  for each connection(response traffic will arive on this port )
for example:
there is a client c1 with ip adress 1.1.1.1
there are three servers
s1(www.bank.com)HTTPS-tcp/443
s2(www.site.com)HTTP-TCP/80
s3(chat server)IRC-UDP/6667
 so the connection looks like this 
c1-src-1.1.1.1:9999(9999 is a rondom port client selcted ) 
dst-3.3.3.3:80
response be like 
dst-1.1.1.1:9999(9999 is a rondom port client selcted ) 
src-3.3.3.3:80
so all connections look like 
TCP 1.1.1.1:8888<->2.2.2.2:443
TCP 1.1.1.1:9999<->3.3.3.3:80
UDP 1.1.1.1:7777<->4.4.4.4:6667

by changing the random number we can connect multiple connections to the same server 
TCP 1.1.1.1:6666<->3.3.3.3:80
TCP 1.1.1.1:9989<->3.3.3.3:80
TCP 1.1.1.1:9999<->3.3.3.3:80

Layer 5,6,7- session,presentation,application
distinction betweem these layers is somewhat vague
other networking models combine these into one layer 
L1-L4 are most important to understand how data flows
TCP/IP MODEL
1.application-osi layer 5,6,7
2.host-host-osi layer 4 
3.internet-osi layer 3
4.network acess-osi layer 1,2 


HOW data moves 
layer5,6,7 combines and sends data to the layer 4 
layer 4 adds a port number to the data this is called SEGMENT
now segment is sent to layer 3 it will add a ip adress to the segment this is called as PACKET
now packet is sent to layer 2 it will add a MAC adress to the packet this is called FRAME
that frame is converted into 1's and 0's and put into the wire
THIS process is called sending-encapsulation

receving-deencapsulation
reverse process:
wire-frame-packet-segment-data
if and only all port ,ip,mac adresses match teh requirements

Network devices operates at specific layers
-L2 devices only look into data gram up to L2 header(switches)
-L3 devices only look into the data gram up to l3 header(routers)

Network protocals operate at specific layers
neither of these are strict  rules-excceptions exist

OSI MODEL is simply a model -not rigid rules eveything adheres to 
-it is conceptualization of what is required for data to flow through the internet 