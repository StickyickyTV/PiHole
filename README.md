# PiHole

*****************************************************************
"""NOIP INSTALLIEREN!!!"""
>>sudo apt-get install build-essential

cd /usr/local/src/
sudo wget http://www.noip.com/client/linux/noip-duc-linux.tar.gz
sudo tar xf noip-duc-linux.tar.gz
cd noip-2.1.9-1/
sudo make install

*******************************************************************
noip2 starten nach jedem Reboot
>>sudo /usr/local/bin/noip2
*******************************************************************

"""PIHOLE!!!"""
>>curl -sSL https://install.pi-hole.net/ | bash
*******************************************************************

"""VPN!!!"""
>>curl -L https://install.pivpn.io/ | bash
*******************************************************************

"""Fritz box!!!"""
>>sudo echo "192.168.178.1 fritz.box" | sudo tee --append /etc/hosts

*******************************************************************
>>SSH installation für Putty: 
sudo apt-get install ssh
*******************************************************************

>>Bestehendem Ordner Rechte geben: sudo chmod -v 777 [ordername]

>>Ordner erstellen mit Rechte: sudo mkdir -m 777 [ordername]

>>Ordner im Verzeichnis löschen: sudo rm -r [Ordner name]

*******************************************************************
"""PIHOLE COMANNDS"""
Pihole -h

*******************************************************************
"""PIVPN COMMANDS"""
pivpn
*******************************************************************

"""JAVA COMMANDS"""
>>Java Version überprüfen: java -version
*******************************************************************

"""Minecraft Server"""
>>Minecraft Server installieren: curl -fsSL https://getmc.marc.tv/ -o install-pi-docker-minecraft.sh 
chmod +x install-pi-docker-minecraft.sh 
./install-pi-docker-minecraft.sh
*******************************************************************

"""Teamspeak server Installieren"""

>>Teamspeak server installieren (MIT automatischem Neustart): sudo docker run -d --name TeamSpeak --restart unless-stopped -e TS_UPDATE=1 -e TS_UPDATE_BACKUP=1 -e TIME_ZONE=Europe/Berlin -p 9987:9987/udp -p 10011:10011/tcp -p 30033:30033/tcp -v /opt/teamspeak/:/teamspeak/save/ ertagh/teamspeak3-server:latest

>>Teamspeak server Logs einsehen: cat /opt/teamspeak/logs/*
*******************************************************************
