# mini_project01_network_setup_and_troubleshooting


# Configuration Guide 

Objective: A network is defined as multiple units that are interconnected and communicate with one another. We are creating a network made up of end servers such as printers, phones, TVs, tablets,and in this configuration: PCs,laptops, and servers. The objective of this network setup is to simulate a network enviornment and configure the devices to communicate with one another and external networks. This practice involves assigning IP addresses, setting up subnet masks, and configuring hardware such as routers, switches, and DNS servers. This should help you understand network concepts and the process of transmitting data across different devices.

Cases for the System: 
 - Accessing a webpage -> Computers communicate through IP addresses, therfore when you want to access a webpage, you type the domain name into google but your computer is using a DNS server to identify which IP address is configured with the webpage. The web server then responds with the webpage content. 
 - Transferring a file -> Similar to accessing a webpage, your laptop sends a request to a DNS server to find the IP Address associated with the domain name and once you have the IP Address, you can request the web server hosting the webpage.
 - Network Printing -> the user sends a print job to the network printer, once the printer on the network is identified, it transfers the print file there, last the printer receives the print file and prints it.  

Steps to Set Up a Network: 
 1) Add the end devices (laptops, PCs, printers, tablets, servers, etc)
- This can be found in packet tracer by selecting "End Devices" in the bottom left corner, and choosing the end devices you want from the box of options to the right. 
 2) Add the switch and connect the switch to the end devices using an ethernet cable (Copper-Straight Through Cable). A switch provides connectivity between hosts within the same local area network (LAN) but not connectivity to other LANs. You can differentiate them from a router because a switch has more ports (so you can connect more end devices to it)
  - This can be found in packet tracer by selecting "Network Devices" from the bottom left corner and choosing switches from the bottom row. To add the cables, choose "Connections" from the bottom left box and the "Copper-Straight Through" cable from the box to the right. To connect the cables, click the switch and choose the first available ethernet port(Fast Ethernet 0 and 1), then click on the end device and do the same steps. Repeat the connection for every end device you have. 
 3) Set up the IPv4 Addresses for the end devices and switches.
- This can be done in packet tracer by clicking on the end devices and going to "Config". Under interface you should see fast ethernet 0, set it to static and input the IPv4 address and subnet mask. It is common practice to prioritize the first available IP Address and Subnet mask for the switch, router, then end devices. In our case, we had the available IP Addresses: 192.168.0.0/26 and 172.16.0.0/24. 192.168.0... is normally used for smaller computers which is why we used it on the PC-based local area network whereas 172.16.0... is normally used for bigger devices like servers. the /24 and /26 represents how many available IP Addresses you have to assign. There is a formula to calculate the possible IP Addresses, you do 32 (for the number of bits) - 24 or 26 (for the number of bits used by the network) and the difference represents bits left for the host of the IP Address. You convert it to binary by doing 2^difference to findthe number of usable IP Addresses. Therefore we have 256 usable IP Addresses for 192.168.0.... and 64 usable IP Addresses for 172.16.0....
- If you want to observe the IP addresses on the end devices by clicking on the end devices and choosing "Desktop" then choosing "Terminal". Once in the terminal, you can use "ipconfig" and clicking enter.
 4) Add a router. The router is automatically off for security purposes so you must set it on. A Router allows end devices on the local area network to talk to other local area networks (sends data over the internet)
- To turn the router on, you click on the router you should see a picture of it, click the power button. You know it is on when you can see a green light on.
 5) Connect an ethernet cable from the switch to the router.
-  To do this on packet tracer, click on the router, go to "Config", choose GigabitEthernet 0/0 (or the one you plugged into) and edit the IP address and subnet mask there. The IP address should be prioritized and a lower number than the end devices.
 6)  Set up the default gateway for all. A default gateway tells the device where to go if the server isn't responding. For servers and PCs the default gateway should be the IP Address of the router so if the server isn't responding, the request can be sent to other local area networks to find a response. If a router has multiple local area networks that it is connected to, each interface is assigned an IP address that acts as the default gateway for the devices on that subnet. Therefore, the router's default gateway should be the switch of the local area network it is trying to access.
- For the switch, router, and end devices, you should be able to manipulate the default gateway by clicking on the device in packet tracer, going to "Config", and updating the default gateway. 
  Extra Steps:
7) Once the network is all set up you can ping the local area network or the other local area networks if the router is connected. This can be done in the terminal by clicking on the end devices and choosing "Desktop" then choosing "Terminal". Once in the terminal, you can use "ping" + the IP of who you are trying to ping. Ping tells you if the device is on the network.
8) Setup a Domain Name Systems (DNS) server and practice using the DNS to open webpages from the browser by entering the device's IP Address or domain name. A DNS server translates the domain name into its associated IP Address to locate the server where the webpage is hosted. This allows the computers to communicate so you can recieve the webpage from the IP Address that is hosting it.
  - On another device or the end device you can download a DNS server such as NAMO(MAMP). In MAMP you will first configure by opening MAMP and navigate to preferences, choose server and select Nginx, then look at port and update the Nginx Port to 80. Last, set the servers on by clicking the right power button. In the directory for your operating system type "/MAMP/htdocs/index.html". You should be able to open this in a code editor like VS Code to configure an index.html page which can be accessed when you access the webpage.
  - Once the webpage is configured and the DNS is running, another device can open a web browser and search for the domain. The request is sent out, the server replies, and searching the IP address or domain name should allow the requesting computer to see the index file created.

 # FAQ 

 ### I plugged in the switch but the ports are not glowing. Is it on?

What to Include:
- Common issues faced during configuration or operation
- Troubleshooting steps for frequent errors
- Best practices
- Tips for maintaining or modifying the system

Filename: Append to the README.md under an FAQ heading.
Length: Minimum of 5 key questions and answers


