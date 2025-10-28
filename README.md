A firewall acts like a security gate between your computer or network and other systems.
It decides whether to allow or block network traffic based on a set of rules.
I have used some basic tools like ufw,firewalld and iptable for flitering the traffic and to add or delete the rules of firewall.

1. Traffic Direction
Firewalls filter traffic in two directions:
Inbound traffic – data coming into your system (for example, SSH or web requests).
Outbound traffic – data leaving your system (for example, browsing the web).

2. Filtering Method
Firewalls inspect each network packet and compare it against their rules.
Rules can check details such as:
IP addresses (source and destination)
Port numbers (for example, 22 for SSH, 80 for HTTP)
Protocols (TCP, UDP, ICMP)
Connection state (new, established, related)

3. Rule Decision
Each packet is tested against the rules in order:
If it matches a rule, the firewall takes that rule’s action:
ALLOW – let it pass
DENY/DROP – block it
If no rule matches, the default policy applies (usually deny).

4. Firewall Types
Type	Works At	Example
Packet-filtering firewall	Network layer	iptables, ufw
Stateful firewall	Tracks connection states	firewalld, Windows Firewall
Application firewall	Application layer	Web Application Firewalls (WAFs)

5. Example Flow
A packet arrives on port 22.
The firewall checks if a rule allows TCP traffic on port 22.
If allowed, the connection is established.
If blocked, the packet is dropped and the connection fails.
