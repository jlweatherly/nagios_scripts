# Various Nagios scripts created by me
====================

Plugins
-------

### check_cpuload

Check the CPU load in SmartOS global zone

    ~ $ ./check_cpuload [-i|-a] -w [warning] -c [critical]
    OK: CPU load: 15%
    
### check_cpuload_linux.sh

Check the CPU load in Linux

    ~ $ ./check_cpuload [-i|-a] -w [warning] -c [critical]
    OK: CPU load: 15%
    
### check_cpuload_mac.sh

Check the CPU load in OS X

    ~ $ ./check_cpuload_mac.sh -w [warning] -c [critical]
    OK: CPU load: 15%

### check_cputemp_freebsd.py

Check the CPU temperature in FreeBSD

    ~ $ ./check_cputemp_freebsd.py -C [core] -w [warning] -c [critical]
    OK: CPU Temperature: 49 C

### check_cputemp_mac.py

Check the CPU temperature in OS X
Requires Temperature Monitor by Marcel Bresink Software-Systeme

    ~ $ ./check_cputemp_mac.py -w [warning] -c [critical]
    OK: CPU Temperature: 46 C

### check_eds_humidityprobe.py

Check humidity probes on EDS 1-wire server

    ~ $ ./check_eds_humidityprobe.py -H [hostname] -p [probe number] -w [warning] -c [critical]
    OK: Humidity: 38.43 %

### check_eds_tempprobe.py

Check temp probes on EDS 1-wire server

    ~ $ ./check_eds_tempprobe.py -H [hostname] -p [probe number] -w [warning] -c [critical]
    OK: Temperature: 5.0 C

### check_hdd_temp.py

Check the temperature of hard drives and calculate a mean value
Requires smartmontools and privileges to check the disk temperatures

    ~ $ ./check_hdd_temp.py -w [warning] -c [critical] [disks to check]
    OK: Temperature: 38 C

### check_smartos_mem.sh

Check the free/used memory status of a SmartOS hypervisor

    ~ $ ./check_smartos_mem.sh -w [used memory warning percent] -c [used memory critical percent]
    OK: Total mem: 24259 MB Free mem: 17264 (72%) MB Used mem: 6995 (28%) MB
    
### check_smarttemp.js

Check the temperature of hard drives and calculate a mean value
Requires smartmontools and privileges to check the disk temperatures

    ~ $ ./check_smarttemp.js [warning temp] [critical temp] [zpool]
    OK: Mean temp: 40 C
    
### check_synology_raid.py

Check the RAID status of a Synology Disk Station
Requires snmpget to check the RAID status

    ~ $ ./check_synology_raid.py -H [Hostname] -C [SNMP Community]
    OK: RAID Status Normal
    
### check_ypool.py

Check the status of number miners online in ypool mining pool

    ~ $ ./check_ypool.py -C [command] -K [API key] -ct [coin type] -w [warning] -c [critical]
    OK: Miners: 2;miners=2
