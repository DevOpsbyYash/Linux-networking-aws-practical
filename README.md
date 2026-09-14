<p align="center">

  <h1 align="center">Linux Networking & AWS Cloud Practical Examination</h1>

  <p align="center">
    Hands-on Linux Networking, IP Addressing & Cloud Troubleshooting
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/OS-Linux-black?style=for-the-badge&logo=linux" alt="Linux">
    <img src="https://img.shields.io/badge/Shell-Bash-green?style=for-the-badge&logo=gnu-bash" alt="Bash">
    <img src="https://img.shields.io/badge/Cloud-AWS-orange?style=for-the-badge&logo=amazon-aws" alt="AWS">
    <img src="https://img.shields.io/badge/Networking-IPv4-blue?style=for-the-badge" alt="IPv4">
  </p>

</p>

---

## About the Project

This project demonstrates practical Linux networking and AWS cloud operations performed as part of a practical examination.

The practical covers important networking concepts including IP address investigation, IPv4 analysis, dynamic IP addressing, AWS EC2 networking, and cloud network troubleshooting.

All practical activities were performed using Linux command-line tools and AWS cloud services where required.

The commands, outputs, screenshots, and final results are documented for each task.

---

## Practical Tasks

| Task   | Topic                         |
| ------ | ----------------------------- |
| Task 1 | Linux IP Investigation        |
| Task 2 | IPv4 Address Analysis         |
| Task 3 | Dynamic IP Investigation      |
| Task 4 | Cloud Linux Server & IP       |
| Task 5 | Cloud Network Troubleshooting |

---

## Linux & Cloud Environment

| Configuration        | Details    |
| -------------------- | ---------- |
| Operating System     | Linux      |
| Shell                | Bash       |
| Cloud Platform       | AWS        |
| Cloud Service        | Amazon EC2 |
| Network Protocol     | IPv4       |
| Remote Access        | SSH        |
| Screenshot Directory | `image/`   |

---

# Architecture

![Linux Networking and AWS Cloud Architecture](./images/architecture.png)

The practical uses a Linux environment for network investigation and an AWS EC2 Linux server for cloud networking and troubleshooting.

---

# Access Linux Environment

### Task

* Access a Linux machine.
* Use the Linux terminal for networking investigation.
* Execute appropriate networking commands.
* Capture screenshots showing the command and output.

### Screenshot
![Linux Server](./images/server.png)

![Linux Terminal](./images/connection.png)

### Result

The Linux environment was successfully accessed and used for performing the networking practical tasks.

---

# TASK 1 — Linux IP Investigation

### Task

* Launch/access a Linux machine and identify its network configuration.
* Find the system's IP address.
* Identify the network interface being used.
* Find the default gateway.
* Find the DNS information.
* Display the complete network configuration.
* Use appropriate Linux commands and document the command and output for every step.

### Commands Used
```
ip addr
ip -br addr
ip route
cat /etc/resolv.conf
```

### Screenshot

![Task 1 - Linux IP Investigation](./images/Q1.png)

### Result

The Linux machine's IP address, network interface, default gateway, DNS information, and network configuration were successfully identified and documented.

---

# TASK 2 — IPv4 Address Analysis

### Task

* Investigate the IPv4 address assigned to the Linux machine.
* Identify the IPv4 address and separate it into its four octets.
* Identify the value of each octet.
* Determine whether the IP is private or public.
* Use appropriate Linux networking commands to investigate the network/host information.
* Find the IP address of at least two other devices or systems accessible from your environment and compare their addresses.

### Commands Used

```
ip -4 addr
ip addr
ip route
hostname -I
getent ahostsv4 google.com
getent ahostsv4 amazon.com
```


### IPv4 Address Analysis

The IPv4 address consists of four octets separated by dots.

For example:

```text
172.31.22.97

Octet 1 = 172
Octet 2 = 31
Octet 3 = 22
Octet 4 = 97
```

The actual IPv4 address obtained during the practical should be used in the final analysis.

### Private IPv4 Address Ranges

```text
10.0.0.0       - 10.255.255.255
172.16.0.0     - 172.31.255.255
192.168.0.0    - 192.168.255.255
```

If the assigned address falls within these ranges, it is a private IPv4 address.

### Screenshot

![Task 2 ](./images/Q2.png)

![Task 2 ](./images/Q2(2).png)

### Result

The IPv4 address assigned to the Linux machine was identified and divided into four octets. The address was analysed to determine whether it was private or public and was compared with the addresses of other accessible systems.

---

# TASK 3 — Dynamic IP Investigation

### Task

* Investigate how dynamic IP addressing behaves on the Linux machine.
* Record the current IP address.
* Check the network connection status.
* Disconnect and reconnect the network, only if your environment safely allows it.
* Check the IP address again.
* Compare the old and new IP addresses.
* Record whether the IP changed.
* Create a terminal-based record showing:

  * Before disconnect → IP Address
  * After reconnect → IP Address

### Commands Used

```
hostname -I
ip -br link 
hostname -I
echo "Old -> 172.31.22.97"
echo "New -> 172.31.22.97"
echo "IP changes  -> No"
echo "Before disconnect -> 172.31.22.97"
echo "After disconnect -> 172.31.22.97"
```

### IP Comparison

| Condition         | IP Address    |
| ----------------- | ----------    |
| Before Disconnect | 172.31.22.97  |
| After Reconnect   | 172.31.22.97  |
| IP Changed        |     No        |

### Screenshot

![Task 3 ](./images/Q3.png)

### Result

The IP address before and after reconnecting the network was recorded and compared. The result shows whether the dynamically assigned IP address changed after the network was reconnected.

---

# TASK 4 — Cloud Linux Server & IP

### Task

* Create an AWS EC2 Linux instance.
* Connect to the VM using SSH.
* Find its private IP from inside Linux.
* Find its public IP.
* Compare the IP information shown in the cloud console with the information shown inside Linux.
* Document all commands used.
* Provide screenshots showing successful SSH access and the VM's IP configuration.

---

## AWS EC2 Instance

An AWS EC2 Linux instance was created using the AWS Management Console.

The instance was accessed remotely using SSH.

### Screenshot

![AWS EC2 Instance](./images/Q4.png)

![Connect to EC2 using SSH](./images/Q4(2).png)

### Commands Used

```
hostname -I
curl -4 ipconfig.me
curl ipconfig.me
history
```

The private IP shown in the AWS console should match the private IP identified from inside the Linux server.

### Screenshot 

![Task 4 ](./images/Q4(3).png)


### Result

The AWS EC2 Linux instance was successfully created and accessed using SSH. The private and public IP addresses were identified from inside the server and compared with the information displayed in the AWS Management Console.

---

# TASK 5 — Cloud Network Troubleshooting

### Task

* You have a Linux cloud server, but a service running on it cannot be accessed.
* Troubleshoot the server systematically.
* Check the IP address.
* Check the network interface.
* Check the default route.
* Check network connectivity.
* Check running services.
* Check listening ports.
* Check firewall/security rules.
* Identify the problem, fix it, and demonstrate that the service is working.
* Document:

  * Problem
  * Command Used
  * Output
  * Cause
  * Solution
  * Final Result

---

### Commands Used

```
hostname -I
sudo service httpd status 
hostname -I
ip addr 
ip route
pind -c 4 8.8.8.8
sudo service httpd status 
ss -tulnp
sudo service httpd start
sudo service httpd status 
curl http://localhost
```

## Check AWS Security Group

The EC2 Security Group was checked to verify that the required inbound port was allowed.

For example, an HTTP service normally requires:

```text
Type       : HTTP
Protocol   : TCP
Port       : 80
Source     : Appropriate source
```

If a custom port is being used, that port must also be allowed in the Security Group.

### Screenshot

![Task 5 ](./images/Q5.png)

![Task 5 ](./images/Q5(2).png)

---

### Result

The cloud server was systematically investigated from the IP configuration to the network interface, default route, connectivity, service status, listening ports, firewall, and AWS Security Group.

---

# Learning Outcomes

Through this practical examination, I gained hands-on experience with:

* Linux IP configuration
* IPv4 addressing
* IPv4 octets
* Private and public IP addresses
* Network interfaces
* Default gateways
* Routing tables
* DNS configuration
* Dynamic IP addressing
* Network connectivity testing
* AWS EC2
* SSH connectivity
* EC2 private and public IP addresses
* Linux service management
* Listening ports
* Firewall configuration
* AWS Security Groups
* Cloud network troubleshooting

---

# Final Result

All five practical tasks were performed using Linux and AWS where required.

The practical covered Linux IP investigation, IPv4 address analysis, dynamic IP investigation, AWS EC2 networking, and systematic cloud network troubleshooting.

The commands and their outputs were documented, and screenshots were captured for the major steps of each task.

---

# Conclusion

This practical examination provided hands-on experience with Linux networking and AWS cloud networking.

I learned how to investigate IP addresses, network interfaces, gateways, DNS, routing, and dynamic IP behaviour.

I also learned how to connect to an AWS EC2 Linux server using SSH, identify private and public IP addresses, and troubleshoot network-related service access problems.

This practical improved my understanding of Linux networking and gave me practical experience with basic AWS cloud network troubleshooting.

---

# Author

**Yash Jain**

**MCA 1st Year Student | Aspiring DevOps Engineer**
