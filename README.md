*To be opened and executed in CISCO Packet Tracer*<br>
<br>

# Computer Networks Project

- A small business network, divided into admin network and guest network, was created using CISCO Packet Tracer
- The total number of admin users allowed is 70 with a maximum of 10 guest users
- An FTP Server with restricted access was also created to demonstrate file sharing across the network
- The guest and LAN network operate on different subnets to allow for separation
<br>

##### IP NETWORK DESIGN TABLE

![image](https://user-images.githubusercontent.com/45356614/141163488-f497d933-c276-44a3-8eec-5deb30f859eb.png)

![image](https://user-images.githubusercontent.com/45356614/141164855-f01ef9ca-a317-43c4-b815-50072db238ab.png)

![image](https://user-images.githubusercontent.com/45356614/141165195-fabf11d3-8ae5-416e-9013-e17e78c3cf05.png)

##### NETWORK CONFIGURATION
> Main Router: <br>
> IP Address: 192.168.10.1 <br>
> Subnet Mask: 255.255.255.0

> Switch <br>
> FastEthernet 0/1 VLAN 1 default (Connected to Main Router) <br>
> FastEthernet 0/2 VLAN 1 default (Connected to Admin Router) <br>
> FastEthernet 0/3 VLAN 3 guest (Connected to Guest Router) <br>

> Admin Router <br>
> DefaultGateway: 192.168.10.1 <br>
> DNS_Server: 192.168.10.1 <br>
> IP: 10.0.0.1 <br>
> Subnet Mask: 255.255.255.0 <br>
> IP Range: 10.0.0.100 – 10.0.0.170 <br>
> SSID: Admin WIFI <br>
> Password: <admin_pswd> <br>

> Guest Router <br>
> DefaultGateway: 192.168.10.1 <br>
> DNS_Server: 192.168.10.1 <br>
> IP: 192.168.0.1 <br>
> Subnet Mask: 255.255.255.0 <br>
> IP Range: 192.168.0.100 – 192.168.0.110 <br>
> SSID: Guest WIFI <br>
> Password: <guest_pswd> <br>

> FTP Server (Admin): <br>
> FastEthernet0 <br>
> DefaultGateway: 10.0.0.1 <br>
> DNS_Server: 192.168.10.1 <br>
> IP (Static): 10.0.0.100 <br>
> Subnet Mask: 255.255.255.0 <br>
> Username: admin <br>
> Password: <admin_pswd> <br>
> Permissions: RWDNL <br>

> FTP Server (Guest): <br>
> FastEthernet1 <br>
> DefaultGateway: 192.168.0.1 <br>
> DNS_Server: 192.168.10.1 <br>
> IP (Static): 192.168.0.100 <br>
> Subnet Mask: 255.255.255.0 <br>
> Username: guest <br>
> Password: <guest_pswd> <br>
> Permissions: RL <br>

> Admin Network Devices: <br>
> DefaultGateway: 10.0.0.1 <br>
> DNS_Server: 192.168.10.1 <br>
> IP: Dynamic <br>

> Guest Network Devices: <br>
> DefaultGateway: 192.168.0.1 <br>
> DNS_Server: 192.168.10.1 <br>
> IP: Dynamic <br>
