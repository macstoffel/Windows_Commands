# Windows_Commands

# [40 Windows Commands you NEED to know](https://www.youtube.com/watch?v=Jfvg3CS1X3A)


## ** Special Thanks to NetworkChuck ** 
Please follow his channel on [YouTube](https://www.youtube.com/c/NetworkChuck)

---

### Simple Commands:

##### Open The Command Prompt: WindowsKey + S

##### Clear Screen:
`> cls`

---
### IP-Address commands

##### Computers IP-Address:
`> ipconfig`

##### Full IP-Address configurations:
`> ipconfig /all`

##### Too much information? Filter with a pipe '|' and findstr:
`> ipconfig /all | findstr DNS`

##### New IP-Address? <- for all interfaces:
`> ipconfig /release`
`> ipconfig /renew`

##### New IP-Address for specific interface:
`> ipconfig /release "Wi-Fi"`

---
### DNS commands

DNS can be a problem... In fact, it's always DNS. It's never the network
Remember that! So let's troubleshoot DNS first

##### Display all the websites it knows:
`> ipconfig /displaydns`

##### Copy above output to the clipboard:
`> ipconfig /displaydns | clip`
now fire-up a texteditor and paste the clipboard... there you go

##### Flush DNS
`> ipconfig /flushdns`

##### nslookup
`> nslookup networkchuck.com`

##### nslookup other DNS-server:
`> nslookup networkchuck.com 8.8.8.8`  <- Google-DNS

##### nslookup MX
`> nslookup -type=mx networkchuck.com`

##### nslookup TXT
`> nslookup -type=txt networkchuck.com`

##### nslookup pointers
`> nslookup -type=ptr networkchuck.com`

Remember above, because: IT'S ALWAYS DNS, never the network!!!

---
### MAC-Address commands

##### Get all MAC-Adresses:
`> getmac /v`

---
### Power Issue commands

##### Power/energy issues:
`> powercfg /energy`

##### Battery issues:
`> powercfg /batteryreport`

---
### File commands

##### which files are associated with wich program:
`> assoc`

##### associate files with a specific program:
`> assoc .mp4=VLC.vlc`

---
### Other Issue commands

##### Check Disk:
`> chkdsk /f`

##### Check Disk for physical sector issues:
`> chkdsk /r`

##### Check system-files:
`> sfc /scannow`

##### Deployment Image Servicing and Management
`> DISM /Online /Cleanup-Image /CheckHealth`

`> DISM /Online /Cleanup-Image /ScanHealth`

`> DISM /Online /Cleanup-Image /RestoreHealth`

After these commands, run a sfc again

---
### TaskLists

##### Tasklist
`> tasklist | findstr script

##### Taskkill
`> taskkill /f /pid 20184`

---
### Net sh

##### Show wireless-LAN report:
`> netsh wlan show wlanreport`

##### Show Interfaces:
`> netsh interface show interface`

##### Show IP-Addresses:
`> netsh interface ip show address | findstr "IP Address"`

##### Show DNS-Servers
`> netsh interface ip show dnsservers`

##### Turn off Windows Defender Firewall:
`> netsh advfirewall set allprofiles state off`

##### Turn on Windows Defender Firewall:
`> netsh advfirewall set allprofiles state on`

---
### PING

##### Check client is up:
`> ping networkchuck.com`

##### keep PING running:
`> ping -t networkchuck.com`

##### TraceRoute:
`> tracert networkchuck.com`

##### TraceRoute speedup:
`> tracert -d networkchuck.com`

---
### NETSTAT

##### What are the connections:
`> netstat`

`> netstat -af`

##### Show process ID for connected processes:
`> netstat -o`

##### Receive statistics every 5 seconds:
`> netstat -e -t 5`

---
### Network Routes

##### Show Routes (gateways) the PC takes:
`> route print`

##### Add Route to PC:
`> route add 192.168.40.0 mask 255.255.255.0 10.7.1.44`

##### Delete route:
`> route delete 192.168.40.0`

---
### ShutDown

##### shutdown and reboot:
`> shutdown -r`

##### Shutdown and reboot into BIOS:
`> shutdown /r /fw /f /t 0`


