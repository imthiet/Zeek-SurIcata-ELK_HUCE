# Zeek-SurIcata-ELK_HUCE

## This is a presentation about an internal network security monitoring system with Zeek + Suricata + ELK. A Lab of me to dig more about Linux System

## IDEA:

- Build a an internal network security monitoring system with: 

    - Suricata: Attack detection based on signatures (IDS)
    - Zeek (Bro): Behavioral analysis, packet capturing
    - Filebeat: Sends logs to Elastic
    - Elasticsearch: Stores searchable logs
    - Kibana: Log analysis dashboard, alerts

- What i will learn after this:
    
    - Network traffic analysis (PCAP)
    - Cyber attack detection (IDS/IPS)
    - In-depth log analysis (SIEM)
    - Real-time log processing and alerting

- Requirement system:
    - Ubuntu 22.04(LTS)
    - Ram: Minimum 4GB
    - At least 2 machine to test traffic form client

## -> Start!!!

- Step 1: Install Suricata

```
sudo apt update
sudo apt install -y software-properties-common
sudo add-apt-repository ppa:oisf/suricata-stable
sudo apt update
sudo apt install -y suricata

```

Result: 

# Zeek-SurIcata-ELK_HUCE

## This is a presentation about an internal network security monitoring system with Zeek + Suricata + ELK. A Lab of me to dig more about Linux System

## IDEA:

- Build a an internal network security monitoring system with: 

    - Suricata: Attack detection based on signatures (IDS)
    - Zeek (Bro): Behavioral analysis, packet capturing
    - Filebeat: Sends logs to Elastic
    - Elasticsearch: Stores searchable logs
    - Kibana: Log analysis dashboard, alerts

- What i will learn after this:
    
    - Network traffic analysis (PCAP)
    - Cyber attack detection (IDS/IPS)
    - In-depth log analysis (SIEM)
    - Real-time log processing and alerting

- Requirement system:
    - Ubuntu 22.04(LTS)
    - Ram: Minimum 4GB
    - At least 2 machine to test traffic form client

## -> Start!!!

- Step 1: Install Suricata

```
sudo apt update
sudo apt install -y software-properties-common
sudo add-apt-repository ppa:oisf/suricata-stable
sudo apt update
sudo apt install -y suricata

```

Result: 

![image](https://github.com/user-attachments/assets/a00bdfea-5b90-4187-b6b6-5bbc92a003ed)

- Step 2: Check Network Config to choose interface(enp0s3,eth0,...)

    `ip addr`

![image](https://github.com/user-attachments/assets/02b4dec7-0fe0-4f0c-92a4-a65e213db240)


- Step 3: Run on test: Suricata:

  `sudo suricata -i ens33`

- Step 4: Check file `/var/log/suricata/fast.log`

`tail -f /var/log/suricata/fast.log`


![image](https://github.com/user-attachments/assets/5af299b3-5949-4241-b2be-6fed5e855aee)


- Step 5: Isntall Zeek( aka Bro before ):
  
```
sudo apt install cmake make gcc g++ flex bison libpcap-dev libssl-dev python3-dev

swig zlib1g-dev

git clone --recursive https://github.com/zeek/zeek

cd zeek

./configure

make -j$(nproc)

sudo make install

```

If any question to continue, input: Y and Enter

![image](https://github.com/user-attachments/assets/144a637d-e7f5-4cc6-95a1-2ce5dc6e944a)


- Tạo Alias:

![image](https://github.com/user-attachments/assets/faa231f6-4651-45e5-9e68-206982e4da47)

- 
- Step 6: Install Elasticsearch:

```
sudo apt install elasticsearch
sudo systemctl enable --now elasticsearch

```

![image](https://github.com/user-attachments/assets/5e2a0010-998b-4955-960b-cfb14ce4d55a)

Result: 



- Step 7: 







