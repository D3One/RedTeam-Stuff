An example of my custom script on the NSE engine for the nmap scanner, once used for a typical express pentest

📕Script features:📕

Detection of known backdoors:
    ✅ Checking ports from the database of known backdoors (31337, 12345, etc.)
    ✅ Signature analysis of banners for popular malware

DNS tunneling:
   ✅ Sending specially crafted DNS requests
   ✅ Response size analysis (abnormally large responses)
   ✅ Use of random long subdomains

Analysis of abnormal behavior of the host's network system:
   ✅ Detection of unusual port combinations
   ✅ TTL check to identify NAT/cloud environments
   ✅ Detection of non-standard services on ports
   ✅ Visual identification of threats:

Report:
   ✅ Ranking by threat level (⚠️, 🛑, 🚨)
   ✅ Clear output structure

Usage:
# Install the script:
sudo cp malware-hunter.nse /usr/share/nmap/scripts/
sudo nmap --script-updatedb

# Start scanning:
nmap -sV -T4 -Pn --script malware-hunter <target>
# Start scanning with “default” options:
nmap -sV --script=malware-hunter.nse target.com

#pentest

