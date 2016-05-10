# The Story of IP 
## Analogy
If we think of the domain name (github.com) as personal name, IP address is like a street address. The fields in an IP address kind of resembles to country, state, city, street, and street number. When one sends a mail, he/she puts the message in an envelope, writes down the address, and then puts the envelope in the nearest mailbox, leaving the task of delivery to the mailman. Supposed the mail is destined to another city, the mailman does not go search for the exact house, he/she simply takes the mail to the local post office, which sends the mail to the right city, where someone knows the street and street number and finishes the delivery.
Since Internet reaches virtually anywhere in the world, users cannot possibly know all the IP address. Fortunately, the Internet keeps a address book in DNS so one can find the someone else's address using domain name. 
## How does one get an IP address
Without an address, one is not able to receive mail. In a similiar fashion, one's IP address tells the Internet to send the information(websites, email...etc) requested to the computer/mobile phone that's being used, but how did one get the IP address in the first place? (it's not like everyone's computer has a domain name) DHCP is the answer. DHCP stands for **dynamic host configuration protocol**. DHCP is in the application layer. Individual's device who needs an IP address (DHCP client) sends request to its DHCP server. A DHCP server with a number of IP addresses at its disposal will lease the requesting client an IP address. In most cases, one's Internet Service Provider is likely to be his/her DHCP server. A typical transaction involves 
1. DHCP discovery
2. DHCP offer
3. DHCP request
4. DHCP acknowledgement
### "Dynamic"
Instead of getting one fixed IP address all the time, most devices get a IP address that is available from a subnet so the IP addresses leased out by DHCP will expire after a certain period of time. 
A DHCP server renews leases automativally, but if renewal doesn't take place in time, the device will be assigned a new IP address. 
## IP Overview
The IP, which stands for **Internet Protocol**, is responsible for addressing hosts and routing datagrams from source to desination host across one or more IP networks. 
IP is a connectionless protocol, is hence an unreliable protocol with no gurantee of reliable delivery, error-free delivery, or ordered delivery. Reliability issues are resolved at upper layer (TCP). 
Currently, both IPv4 and IPv6 are deployed. 
## IPv4
IP version 4 uses 32-bit(4 byte) addresses, limiting the address space to 2<sup>32</sup>. (actually less than this number because some spaces are reserved for special uses, like 224 is reserved for multicast addressing) 
## Scaling
In the old days, classful addressing struture was used to assign address, but it had scaling problems with the exponential growth of connected hosts around the world. It soon ran out of IP addresses and capacity in the routing tables. 
### CIDR
In the routing table, one routing prefix can represent a hugh chunk of network addresses.
#### Longest prefix match
## IPv6
## Intra-domain routing
### Distance vector routing
### Link state routing
## BGP - the glue of all IPs
## IP mobility
Consider the scenario when a mobile device user moves from one network to another, how can the device maintain its active session? Mobile IP (RFC3320) is the solution to ensure that mobility is transparent to the application layer. The mobile unit needs to be able to maintain a **home address** regardless of its current location. An analogy is that one's cellphone number remains the same when traveling from one country to another country. 
### Mobile IP architecture and vocabulary
![Image of mobile IP architecture]
(http://www.cisco.com/c/dam/en/us/td/i/000001-100000/50001-55000/53001-53500/53030.ps/_jcr_content/renditions/53030.jpg)
###### Home network
is the network where the mobile node receives its assigned IP address. 
#### Home address
is the IP address assigned to the mobile node at the home network
#### Home agent
is the entity on the home network responsible for tunneling the packets destined to the mobile node when it's away.
#### Foreign network
is the network where the mobile node currently resides. 
#### Care-of address
is the network-native IP address assigned to the mobile node when it's in a foreign network.
#### Foreign agent
is the entity that holds the mapping of care-of addresses and home addresses. 
### Operation
The approach is to let the routers act as middle-men and handle the mobility issue through either **indirect routing** or **direct routing**.
#### Agent discovery
##### Agent solicitation
##### Agent advertisement
#### Mobility registration
#### Indirect routing (triangular routing)
#### Direct routing

## VPN
