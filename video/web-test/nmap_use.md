# Nmap use

## Tools

- [Nmap](https://nmap.org/)

### Nmap

function : Network exploration tool and security / port scanner

#### arguments

- `-sS` : TCP SYN scan
- `-sT` : TCP connect scan
- `-sU` : UDP scan
- `-sV` : Version detection
- `-O` : OS detection
- `-A` : Aggressive scan
- `-p` : Port scan
- `-T` : Timing template

eg. `nmap web.antgst.com -sV -O ` result : 

``` plaintext
TCP/IP fingerprinting (for OS scan) requires root privileges.
QUITTING!
```

#### script

- `nmap -sV --script=vuln <target>` : Vulnerability scan
- `nmap -sV --script=exploit <target>` : Exploit scan

# hydra

for brute force attack

``` bash
hydra -l <username> -P <password list> <target> <service>
```

eg. `hydra -l admin -P /usr/share/wordlists/rockyou.txt