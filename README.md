# masscan-openVPN
Fixing - Error: bad packet template :-)
```
wget https://github.com/scriptzteam/masscan-openVPN/blob/main/src/templ-pkt.c  
mv templ-pkt.c into your /masscan/src/ folder  
make  
make install  
```  
Test:
```
openVPN ip - 1.2.3.4  
real server ip - 5.6.7.8  
```
Get your router ip
```
ip route
```

Sample:  
```masscan 9.10.11.12 -p22 -e tun0 --router-ip 10.8.0.1```
  
In ```tcpdump port 22``` on scanned server with masscan is openVPN ip :-)
