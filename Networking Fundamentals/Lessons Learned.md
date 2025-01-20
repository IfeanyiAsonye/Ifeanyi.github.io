Resource Used - https://www.youtube.com/watch?v=iSOfkw_YyOU&t=9020s - By Abhishek veeramalla

*Concepts*
IP Address
I now understand ip addresses to mean some sort of identifier ID for devices connected in a 
network. You know how you have particular arears in superstore labelled, eg Cosmetics, Groceries etc.
so see those areas as devices interconnected in the entire building. This might be a very port analogy 
but here's where am i going with this, i am trying to say is that, for all devices conneted to a network, they 
what is called IP address. That's the only way you can use, share and recieve anything over that network.
types of IP addresses are IPV4 (what you'll mostly work with) and IPV6(this one is massively large, don't borther too much about it, you might never have to use 'em) 

SUBNET
Full menaning "subnetwor". This is one step down the ip address. it simply means a logical subdivision of the 
larger IP network. I kinda feel like sometimes, this is influence by structure - it may be physical or organisational but 
these are my opinion. Although some other things go on under ther hood but i'll only write on the important one - CIDR 
CIDR - Means classeless interdomain routing i guess but here what you need to know about it, its an allocation method. 
if you have experince working on-prem infra you might have heard of DHCP. Yeah, this is somehow linked to that but i wont be 
writing about that, just know that it is a way to know how many IP addresses can be assigned in a subnet. 

PORTS
I understand ports to be virtual point where entry and exit to only a particular service can happen. 
kinda like the door or window to a particular room in a house where you don't actually enter the house.
There are many out there you don't need to learn them all, just know a couple like the ssh, FTP, TCP, HTTP. 


OSI MODEL
This is an important concept, you cannot skip it, if not you'll keep coming back to it so know it and have peace. 
There are 7 layers sometimes read as 7-1 or 1-7, it doesn't matter. 
Although in the youtube video refrence, he touched on DNS resolution, TCP handshake and the data movement lifecycle i.e sending and recieving
Here is a summary
- Application Layer - Https request (Browser request)
- Presentation Layer - formating and encription
- Session Layer - ensure that you don't loose an already established connection
- Segmentation Layer - speaks to how they are transported (TCP and UDP). Some internet memes can explain this better
- Network Layer - Interactions on the router (packets and IPs)
- Data Layer - Switch working (packet become frames - Here we do MAC address) 
- Physical Layer - Cables and all


VPC OVERVIEW IN AWS CONSOLE
- How networking is done in the cloud, security measures like security groups, NACL (Network access control list), NAT gatways, route tables and load balancers. 

I got to experiment using the AWS Educate Networking Lab Simulation fr try outs. 