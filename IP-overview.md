# The Story of IP 
## Analogy
If we think of the domain name (github.com) as personal name, IP address is like a street address. The fields in an IP address kind of resembles to country, state, city, street, and street number. When one sends a mail, he/she puts the message in an envelope, writes down the address, and then puts the envelope in the nearest mailbox, leaving the task of delivery to the mailman. Supposed the mail is destined to another city, the mailman does not go search for the exact house, he/she simply takes the mail to the local post office, which sends the mail to the right city, where someone knows the street and street number and finishes the delivery.
Since Internet reaches virtually everywhere in the world, users cannot possibly know all the IP address. Fortunately, the Internet keeps a address book in DNS so one can find the someone else's address using domain name. 
## Overview
The IP, which stands for Internet Protocol, is responsible for addressing hosts and routing datagrams from source to desination host across one or more IP networks. 
IP is a connectionless protocol, is hence an unreliable protocol with no gurantee of reliable delivery, error-free delivery, or ordered delivery. Reliability issues are resolved at upper layer (TCP). 
Currently, both IPv4 and IPv6 are deployed. 
## IPv4
IP version 4 uses 32-bit(4 byte) addresses, limiting the address space to 2<sup>32</sup>. (actually less than this number because some spaces are reserved for special uses, like 224 is reserved for multicast addressing) 
## IPv6
## IP mobility
Consider the scenario when a mobile device user moves from one network to another, how can the device maintain its active session? Mobile IP (RFC3320) is the solution to ensure that mobility is transparent to the application layer. The mobile unit needs to be able to maintain a **home address** regardless of its current location. An analogy is that one's cellphone number remains the same when traveling from one country to another country. 
### Mobile IP architecture and vocabulary
![Image of mobile IP architecture]
(http://www.cisco.com/c/dam/en/us/td/i/000001-100000/50001-55000/53001-53500/53030.ps/_jcr_content/renditions/53030.jpg)
#### Home network
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
#### Agent discovery
##### Agent solicitation
##### Agent advertisement
#### Mobility registration
#### Indirect routing (triangular routing)
#### Direct routing

## VPN
