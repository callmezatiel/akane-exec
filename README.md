# akane-exec
Clone Type-DOS


<details open>
    <summary><b>Resource Development</b> 11 tools</summary>
    <ul>
        <ul>
            <li><b><a href="#chimera">Chimera</a></b><i> PowerShell obfuscation</i></li>
        </ul>
    </ul>
</details>

<details open>
    <summary><b>Reconnaissance</b> 20 tools</summary>
    <ul>
        <ul>
            <li><b><a href="#dismap">Dismap</a></b><i> Asset discovery/identification</i></li>
        </ul>
    </ul>
</details>

### [🔙](#tool-list)[Dismap](https://github.com/zhzyker/dismap)

Dismap is an asset discovery and identification tool. It can quickly identify protocols and fingerprint information such as web/tcp/udp, locate asset types, and is suitable for internal and external networks.

Dismap has a complete fingerprint rule base, currently including tcp/udp/tls protocol fingerprints and 4500+ web fingerprint rules, which can identify favicon, body, header, etc.

**Install:** 

Dismap is a binary file for Linux, MacOS, and Windows. Go to [Release](https://github.com/zhzyker/dismap/releases) to download the corresponding version to run:

```bash
# Linux or MacOS
chmod +x dismap-0.3-linux-amd64
./dismap-0.3-linux-amd64 -h

# Windows
dismap-0.3-windows-amd64.exe -h
```

**Usage:** 

```bash
# Scan 192.168.1.1 subnet
./dismap -i 192.168.1.1/24

# Scan, output to result.txt and json output to result.json
./dismap -i 192.168.1.1/24 -o result.txt -j result.json

# Scan, Not use ICMP/PING to detect surviving hosts, timeout 10 seconds
./dismap -i 192.168.1.1/24 --np --timeout 10

# Scan, Number of concurrent threads 1000
./dismap -i 192.168.1.1/24 -t 1000
```
