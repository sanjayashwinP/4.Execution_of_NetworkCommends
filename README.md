# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

DEVELOPED BY :SANJAY ASHWIN P     
REG NO:212223040181      

## PROGRAM 
## PING COMMAND

## CLIENT:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
## SERVER:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```    

## Output
## CLIENT
![image](https://github.com/sanjayashwinP/4.Execution_of_NetworkCommends/assets/147473265/18818903-e4bc-42c6-a54e-464e5019f9a5)

## SERVER
![image](https://github.com/sanjayashwinP/4.Execution_of_NetworkCommends/assets/147473265/61662956-c55d-4e0b-917e-f358b3edbc93)

## TRANCEROUTE COMMAND:
```
from scapy.all import*     
target = ["www.google.com"]     
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## OUTPUT
## TRANCEROUTE COMMAND
![image](https://github.com/sanjayashwinP/4.Execution_of_NetworkCommends/assets/147473265/b0c8005d-2f8f-45c3-8eb6-bd2f8bdd1af0)

## Result
Thus Execution of Network commands Performed 
