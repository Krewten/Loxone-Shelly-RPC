-----------------------
Configuration on Shelly
-----------------------
( For sending updates to Miniserver )
Set IP and port of Miniserver on Shelly

http://$ShellyIP$/rpc/Sys.SetConfig?config={"rpc_udp":{"dst_addr":"$MiniserverIP$:$Port$"}}

$ShellyIp$ = IP address of Shelly device
$MiniserverIP$ = IP address of Locone Miniserver
$Port$ = Port you use on your miniserver to receive udp data

---------------------------
Configuration on Miniserver
---------------------------
( Receiving updates from Shelly )

Load desired template in loxone (listed above).

Update the Sender Address to the $ShellyIp$ and UDP receive port to the $Port$

Data should start flowing in when saving to miniserver.



