# Find ip of a machine #
### every machine need to be in same network ###

## Tools needed ##
- nmap 
- netdiscover

## Steps ##
- find available ip that in same network by netdiscover
```
netdiscover -r personal_ip/mask
```
- Then find the available port with nmap
```
nmap -sV -O target_ip/mask
``` 
- To access a machine from another machine i.e 'Kali to metasploitable2 machine', need to set the 
1. Set network adapter in NAT Network (For virtualbox)
2. Set network to NAT (For VMWare)