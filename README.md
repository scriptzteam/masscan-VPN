# masscan-openVPN
Fixing - Error: bad packet template :-)
```
cd masscan/src
rm templ-pkt.c
rm proto-http.c
wget https://raw.githubusercontent.com/scriptzteam/masscan-openVPN/main/src/templ-pkt.c
wget https://raw.githubusercontent.com/scriptzteam/masscan-openVPN/main/src/proto-http.c
cd ../
make  
make install  
```

# User-Agent is set in proto-http.c
```
pOrT.sCaNnInG.iS.nOt.A.cRiMe
```

# Test:
```
openVPN ip - 1.2.3.4  
real server ip - 5.6.7.8  
```

# Get your router ip
```
ip route
```

# Sample:  
```
masscan 9.10.11.12 -p22 -e tun0 --router-ip 10.8.0.1
```
  
In ```tcpdump port 22``` on scanned server with masscan is openVPN ip :-)
