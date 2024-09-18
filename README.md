# mini_project01_network_setup_and_troubleshooting


# Configuration Guide 

Objective: A network is defined as multiple units that are interconnected and communicate with one another. We are creating a network made up of end servers such as printers, phones, TVs, tablets,and in this configuration: PCs,laptops, and servers. The objective of this network setup is to simulate a network enviornment and configure the devices to communicate with one another and external networks. This practice involves assigning IP addresses, setting up subnet masks, and configuring hardware such as routers, switches, and DNS servers. This should help you understand network concepts and the process of transmitting data across different devices.

Cases for the System: 
 - Accessing a webpage -> Computers communicate through IP addresses, therfore when you want to access a webpage, you type the domain name into google but your computer is using a DNS server to identify which IP address is configured with the webpage. The web server then responds with the webpage content. 
 - Transferring a file -> Similar to accessing a webpage, your laptop sends a request to a DNS server to find the IP Address associated with the domain name and once you have the IP Address, you can request the web server hosting the webpage.
 - Network Printing -> the user sends a print job to the network printer, once the printer on the network is identified, it transfers the print file there, last the printer receives the print file and prints it.  

Steps to Set Up a Network: 
 1) Add the end devices (laptops, PCs, printers, tablets, servers, etc)
This can be found in packet tracer by selecting "End Devices" in the bottom left corner, and choosing the end devices you want from the box of options to the right. 
 2) Add the switch and connect the switch to the end devices using an ethernet cable (Copper-Straight Through Cable).
This can be found in packet tracer by selecting "Network Devices" from the bottom left corner and choosing switches from the bottom row. To add the cables, choose "Connections" from the bottom left box and the "Copper-Straight Through" cable from the box to the right. To connect the cables, click the switch and choose the first available ethernet port(Fast Ethernet 0 and 1), then click on the end device and do the same steps. Repeat the connection for every end device you have. 
 3) Set up the IPv4 Addresses for the end devices and switches.
This can be done in packet tracer by clicking on the end devices and going to "Config". Under interface you should see fast ethernet 0, set it to static and input the IPv4 address and subnet mask. It is common practice to prioritize the first available IP Address and Subnet mask for the switch, router, then end devices. In our case, we had the available IP Addresses: 192.168.0.0/26 and 172.16.0.0/24. 192.168.0... is normally used for smaller computers which is why we used it on the PC-based local area network whereas 172.16.0... is normally used for bigger devices like servers. the /24 and /26 represents how many available IP Addresses you have to assign. There is a formula to calculate the possible IP Addresses, you do 32 (for the number of bits) - 24 or 26 (for the number of bits used by the network) and the difference represents bits left for the host of the IP Address. You convert it to binary by doing 2^difference to findthe number of usable IP Addresses. Therefore we have 256 usable IP Addresses for 192.168.0.... and 64 usable IP Addresses for 172.16.0....
 4) 
 5) 
 

For IP in End Devices: go to config, Under interface you should see fast ethernet 0, set it to static and input the IPv4 address and subnet (ihow we chose) we choose (why) 
 Add a router to talk to other networks (sends data over the internet), it is ato off for security purposes so you must set it on: when you click on the router you should see a picture of it, click the power button 
Connect an ethernet cable from the switch to the routher, set up the IPv4 address and subnet mask for the router
               On the router: click on the router, config, GigabitEthernet 0/0 (the one you plugged into) edit the IP and subnet there 
 Set up the default gateway for all (why) 

- Detailed steps for setting up core system components (network devices, cloud services, security configurations)
- Screenshots or command outputs to enhance clarity
- Key configuration decisions and justifications

Use 192.168.0.0/26 and 172.16.0.0/24 as the network ranges. Pay attention to the subnet mask for each subnet.


