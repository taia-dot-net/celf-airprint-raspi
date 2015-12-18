#Install raspbian

on OS X 

* insert SD-card into the mac
* find the device with 

	diskutil list

on my machine: 

	/dev/disk2
   		#:                       TYPE NAME                    SIZE       IDENTIFIER
   		0:     FDisk_partition_scheme                        *31.9 GB    disk2
   		1:             Windows_FAT_32 NO NAME                 31.9 GB    disk2s1




After first boot, allow ssh server
first, connect via ssh with IP address, because name resolution might not work, yet

Connecting a printer

Install `cups` 

		sudo apt-get update
		sudo apt-get upgrade (maybe)
		sudo apt-get install cups

			Answer: Y 


		sudo usermod -a -G lpadmin pi
		or sudo addgroup pi lpadmin 


cups will also install bonjour client avahi

Adding "ServerAlias *" to /etc/cups/cupsd.conf

create a backup for cupsd.conf

copy the two files
	cups.service to /etc/avahi/services
	cupsd.conf to /etc/cups

change access rights on cups.service to g+r and o+r

restart cups


##Issues

halting the raspberry pi does not remove the advertised bonjour service. 
So the servcie is still visible in safari or celfCloud Browser even if raspi has been shutdown. 
Maybe the utilities help here. What about advertising via node or python? 





## build essentials

	apt-get install build-essential
	
I assume, this package is required to compile native node modules, like mdns
	