# available-ip
This script uses ping to fetch the remaining available IP addresses in the local network. You can specify the local network, the number of IP addresses to fetch, and whether consecutive IP addresses are required.

## Usage

### Show help message
```bash
available-ip -h
```
![](https://github.com/llnut/available-ip/blob/master/img/help.png?raw=true)

### Fetch from given network
Subnet masks support both the traditional representation and the CIDR representation.
```bash
available-ip -n 192.168.10.1/24
```
or
```bash
available-ip -n 192.168.10.1/255.255.255.0
```
![](https://github.com/llnut/available-ip/blob/master/img/given_network.png?raw=true)


### Fetch a specified number of IP addresses
The following command retrieves five IP addresses from the 192.168.10.1/24 network.
```bash

available-ip -n 192.168.10.1/255.255.255.0 5
```
![](https://github.com/llnut/available-ip/blob/master/img/number2.png?raw=true)

If the number is specified as 0, all available IP addresses will be fetched.
```bash
available-ip -n 192.168.10.1/255.255.255.0 0
```

![](https://github.com/llnut/available-ip/blob/master/img/number.png?raw=true)

### Fetch consecutive IP addresses
The following command retrieves two consecutive IP addresses from the 192.168.10.1/24 network.

```bash
available-ip -n 192.168.10.1/255.255.255.0 -c true 2
```
![](https://github.com/llnut/available-ip/blob/master/img/consecutive.png?raw=true)

### Fetch timeout for each reply.
The following command sets the timeout for single IP fetch to 2 seconds.
```bash
available-ip -t 2
```

## License
[MIT](LICENSE) © llnut
