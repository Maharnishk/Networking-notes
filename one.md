Host:
 hosts are any devices which sends or receive traffic
 ex-computer lapotp phones printers servers cloud server 
 also any IOT devices are called hosts ex-tv speakers lights thermometers smart wathces refridgeratr
Client:
which intiate the request 
Server:
which respond to teh request
both are relative to specific communication
 for example incase the server wants to updates its files it have to pass a request from itslef to file serve so then the server it slef becomes client and the file server becomes the main server
Server:
servers are simply computers with software installed which responds to  specific requests  
IP adress:
it is teh identity of the each host 
72.42.128.15(clinet)------->136.22.17.98(server)
the msg contains the src as cleint ip adress and destination as server ip adress
72.42.128.15(server)<-------136.22.17.98(client)
now 136... becomes client because it is making a request and 72... becomes the server which is responding to request 
ip adresses are 32 bits (every ip adress is diff combination of 32 1's and 0's)
10001000000101100001000101100010(136.22.17.98)
bit = 1 or 0
and represented as four octets
1000 1000 0001 0110 0001 0001 0110 0010
and these octets are converted into decimals ( u can only get the numbers between 0-255 becuase teh maximum number u can get with a 4 binary slots )
136.22.17.98
and these are hierarchically assigned 
for example 10.x.x.x is  a ACME CO-opereation
newyork-10.20.x.x
inside newyork they will have teams like
 sales-10.20.55.x
 engineering -10.20.66.x
 marketing-10.20.77.x
london -10.30.x.x
inside london  they will have teams like
 sales-10.30.55.x
 engineering -10.30.66.x
 marketing-10.30.77.x
tokyo-10.40.x.x 
inside tokyo  they will have teams like
 sales-10.40.55.x
 engineering -10.40.66.x
 marketing-10.40.77.x

this allows to pin point where the particular host exist for example if the ip given is 10.30.55.127 then it must be in acme london sales department
this process is called subnetting

Network:
a network is what transport traffic between hosts
anytime u connect two hosts you have a network
c1-----------(network)-------------c2
before networks 
transferring data between hosts requires portable media like drives disks etc
it is a logical grouping od hosts which require similar connectivity 
home might have laptops printer phone and tablets connected to home wifi
coffe shop have laptop mobile and phone  connected to its wifi
a school might have multiple clasrroms connected to different wifi 
-networks can contain other networks 
sometimes called subnetworks or sub nets ex-school
adn also our acme co-operation
networks connct to other network 
--scenario:
 if u wanna acess to school network files while sitting in a coffe shop it feels not possible that is why all teh netwroks are finnaly connected to internet with the help of internet we can connect to any netwrok we know 
INTERNET:inter connected networks
--------------------------------------------------------