This project demonstrates scanning a local network for live hosts and open ports using Nmap (optional Wireshark/tshark captures). The goal is to identify network exposure and document findings safely. Scan only authorized networks.

Contents

nmap/ — Nmap outputs (.nmap, .xml, .html)

scripts/ — scan scripts 

Usage

sudo nmap -sn 192.168.1.0/24 -oN nmap/hosts_up.txt
sudo nmap -sS -T4 192.168.1.0/24 -oN nmap/syn_scan.txt
xsltproc nmap/full_scan.xml -o nmap/full_scan.html
