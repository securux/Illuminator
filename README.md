# Illuminator

Illuminator is a Python based, OSCP inspired script that is designed to perform a comprehensive scan on a single IP using the tools that are listed below to save time when attempting to gather information on the specific host. As time goes by, I will update the script and add more features and capabilities. It's not perfect, but gotta start somewhere :)

*Nmap*  
*Nikto*  
*Fierce*  
*NBTScan*  
*GoBuster*  
*SNMPcheck*  
*Enum4Linux*  

Illuminator will start with an Nmap scan and generate a folder which will contain a text file with the results from each of the tools utilized. Depending on which ports and protocols are open, and the services that are running on those ports,  Illuminator will utilize the next tool from the list based on those ports and attempt to shed light on more information to assist you in the host enumeration process.

All the listed tools should already be available in **Kali Linux**

You will need to install **python-nmap** using pip to aid in using Nmap with Python, along with Nmap libraries for parsing, in case you get a "libnmap.parser" error if you don' already have it installed.

`pip install python-nmap`

`pip install python-libnmap`

If for some reason that doesn't work, you can manually download it from **[here](https://xael.org/pages/python-nmap-en.html)** and install it.

For **SNMPCheck** you can download it from **[here](http://www.nothink.org/codes/snmpcheck/index.php)** and copy or move it to /usr/bin/ so it can be available from anywhere in the terminal.

For **GoBuster**, I am using `/usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt` for the wordlist, but you can use any list you like; just edit the code to include the the location.

For **SMTP** enumeration using the Nmap NSE, I am using `/usr/share/metasploit-framework/data/wordlists/unix_users.txt` for the wordlist but use whatever you like, just edit the code and place the location of your wordlist.

### Run the script
`./Illuminator.py <ip address>`

### Example
![image](https://user-images.githubusercontent.com/22828882/44691637-7223d000-aa2d-11e8-9729-094cc0569a12.png)

###	Soon to Add
*TBD*
