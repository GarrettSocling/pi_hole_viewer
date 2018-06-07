# pi_hole_viewer

Pihole API Terminal Parsing

This script will show live stats from the Pi-Hole in a terminal.
Hostname resolution will work if the Pi-Hole is used as DHCP server.

![alt text](https://i.imgur.com/v828Ak1.png)

Installation:

```
apt install python3 python3-pip
pip3 install requests

If upgrading From Pi-hole ~3.1 to FTLDNS:

cd /etc/.pihole
sudo git fetch --all && sudo git checkout master
cd /etc/pihole
sudo git fetch --all && sudo git checkout master
echo "FTLDNS" | sudo tee /etc/pihole/ftlbranch
pihole checkout core FTLDNS
pihole checkout web FTLDNS

Finally:

echo "FTLDNS" | sudo tee /etc/pihole/ftlbranch
pihole checkout core FTLDNS
pihole checkout web FTLDNS
```
usage: main.py [-h] [-w WEBPASSWORD] [-i IP]

optional arguments:
  -h, --help            show this help message and exit
  -w WEBPASSWORD, --webpassword WEBPASSWORD
                        WEBPASSWORD (found via cat /etc/pihole/setupVars.conf)
  -i IP, --ip IP        IP address of the Pi-Hole server
```

(You can also provide the WEBPASSWORD in WebPassword.txt)
    
