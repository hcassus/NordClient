# NordClient
A really badly written way to conect to NordVPN

# Disclaimer
This client is completely independent and has absolutely no official connection to NordVPN

This was written for personal use, but feel free to fork, improve or even open PRs

# Requirements
It's difficult to track, so if anything is not present in your distro let me know so I can add here gradually

UFW

OpenVPN


# Executing
Although it sucks big time, by now the client has to be run from /opt/nordclient, and I suggest adding the folder to your PATH. So it becomes easier to use it.

In the auth folder write your username and password in the auth file. I recomment you to ser the permissions to 400 to avoid unwanted access

When connected to a network, the client will block all incoming and outgoing traffic except the one through the tunnel 

The possible commands are:


nord update - Downloads the definitions and enables them to be authenticated by the auth file


nord connect - Connects to the fastest server it can find. If it can't find, it'll grab the first one it finds (most likely in Albania)


nord connect <country_code> - Connects to the fastest server it can find, or the first one for that country.


nord connect <country_code> <tcp|udp>- Connects to the fastest server it can find, or the first one for that country and protocol.


nord disconnect - Kills all openvpn client and restore connectivity out of the tunnel


nord status - Shows what definition is used to connect and the firewall rules in place


nord reconnect - tries to reconnect to the current active connection. This is useful due to the many reports of the inability to reconnect automatically from OpenVPN, while keeping the traffic shut to avoid leaking requests.
