HandShaker
==========
handshaker - Detect, deauth, capture and crack WPA/2 handshakes
	       - Record AP location with Android GPS over adb
		
	Usage: 	handshaker <Method> <Options>
		
		Method:
			-a - Autobot or wardriving mode
			-e - Search for AP by partial unique ESSID
			-l - Scan for APs and present a target list
			-c - Crack handshake from pcap
			
		Options:
			-i  - Wireless Interface card
			-i2 - Second wireless card (better capture rate)
			-w  - Wordlist to use for cracking
			-o  - Save handshakes to custom directory
			-d  - Deauth packets sent to each client (default 1)
			-p  - Only attack clients above this power level
			-g  - Use android GPS to record AP location
			-b  - Use evil twin AP to capture handshakes
			-m  - Use mdk3 for deauth (default aireplay-ng)
			-t  - Attempts to capture per AP (default 3)
			-s  - Silent
			-h  - This help

		Examples: 
			 handshaker -a -i wlan0 -t 5			       ~ Autobot mode on wlan0 and attempt 5 times.
			 handshaker -e Hub3-F -w wordlist.txt	 	   ~ Find AP like 'Hub3-F' and crack with wordlist.
			 handshaker -l -o out/dir			           ~ List all APs and save handshakes to out/dir.
			 handshaker -c handshake.cap -w wordlist.txt   ~ Crack handshake.cap with wordlist.
