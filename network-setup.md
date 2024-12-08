# Network setup

### Devices and their IP Addresses

### Routers

#### Router0(Model: 2811)
- interface Fa0/0 -> 168.90.0.1 (IP address)
- interface Fa0/1 -> 210.3.14.1 (IP address)

### Switches

- Switch0(Model: 2960/2960-24TT)
- Switch1(Model: 2960/2960-24TT)

### Hosts/Devices

#### Left side (Connected to first switch)
- PC0 -> 168.90.0.1 (IP address)
- PC1 -> 168.90.0.3 (IP address)
- Laptop0 -> 168.90.0.4 (IP address)
- Server0 -> 168.90.0.5 (IP address)
- PC5 -> 168.90.0.6 (IP address)

#### Right side (Connected to second switch)
- Server1 -> 210.3.14.2 (IP address)
- Server2 -> 210.3.14.3 (IP address)
- PC2 -> 210.3.14.4 (IP address)
- PC4 -> 210.3.14.5 (IP address)

### DHCP commands explanation

#### Configuring router interfaces

- Router> enable (This command grants access to more advanced commands to the user)
- Router> configure terminal (This command enables router configuration)
- Router> interface fa0/0 (This command specifies configuration just for the Fast Ethernet 0/0 interface)
- Router> ip address 168.90.0.1 255.255.0.0 (This command assigns IP address 168.90.0.1 with the subnet mask 255.255.0.0 to the Fast Ethernet 0/0 interface)
- Router> no shutdown (This command activates the interface)
- Router> exit (This command exits the current configuration mode)
- Router> interface fa0/1 (This command specifies configuration just for the Fast Ethernet 0/1 interface)
- Router> ip address 210.3.14.1 255.255.255.0 (This command assigns IP address 210.3.14.1 with the subnet mask 255.255.255.0 to the Fast Ethernet 0/1 interface)
- Router> end (This command exits global configuration mode)
- Router> write memory (This command saves the current configuration)

#### References

- [How to configure DHCP](https://computernetworking747640215.wordpress.com/2018/07/05/how-to-configure-dhcp-server-in-packet-tracer/)