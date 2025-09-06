# Prometheus Node Exporter System Metrics

This table lists all system metrics that the Prometheus node exporter captures, organized by metric name, supported operating systems, and data sources.

## Metrics Table

| Metric | Supported OS | Source | Status |
|--------|-------------|--------|--------|
| arp | Linux | `/proc/net/arp` | Enabled by default |
| bcache | Linux | `/sys/fs/bcache/` | Enabled by default |
| bonding | Linux | Linux bonding interfaces | Enabled by default |
| boottime | Darwin, Dragonfly, FreeBSD, NetBSD, OpenBSD, Solaris | `kern.boottime` sysctl | Enabled by default |
| btrfs | Linux | Btrfs filesystem statistics | Enabled by default |
| buddyinfo | Linux | `/proc/buddyinfo` | Disabled by default |
| cgroups | Linux | Cgroups filesystem | Disabled by default |
| conntrack | Linux | `/proc/sys/net/netfilter/` | Enabled by default |
| cpu | Darwin, Dragonfly, FreeBSD, Linux, Solaris, OpenBSD, AIX | `/proc/stat`, `/proc/cpuinfo`, sysfs | Enabled by default |
| cpu_vulnerabilities | Linux | `/sys/devices/system/cpu/vulnerabilities/` | Disabled by default |
| cpufreq | Linux, Solaris | `/sys/devices/system/cpu/*/cpufreq/`, sysfs | Enabled by default |
| devstat | Dragonfly, FreeBSD | Device statistics | Disabled by default |
| diskstats | Darwin, Linux, OpenBSD, AIX | `/proc/diskstats`, sysfs, device statistics | Enabled by default |
| dmi | Linux | `/sys/class/dmi/id/` | Enabled by default |
| drbd | Linux | DRBD statistics | Disabled by default |
| drm | Linux | `/sys/class/drm/`, sysfs DRM | Disabled by default |
| edac | Linux | EDAC error detection and correction | Enabled by default |
| entropy | Linux | `/proc/sys/kernel/random/entropy_avail` | Enabled by default |
| ethtool | Linux | `ethtool` network interface information | Disabled by default |
| exec | Dragonfly, FreeBSD | Execution statistics | Enabled by default |
| fibrechannel | Linux | `/sys/class/fc_host/` | Enabled by default |
| filefd | Linux | `/proc/sys/fs/file-nr` | Enabled by default |
| filesystem | Darwin, Dragonfly, FreeBSD, Linux, OpenBSD, NetBSD, macOS | Filesystem mount points and usage | Enabled by default |
| hwmon | Linux | `/sys/class/hwmon/` | Enabled by default |
| infiniband | Linux | InfiniBand and Intel OmniPath statistics | Enabled by default |
| interrupts | Linux, OpenBSD | `/proc/interrupts` | Disabled by default |
| ipvs | Linux | `/proc/net/ip_vs`, `/proc/net/ip_vs_stats` | Enabled by default |
| ksmd | Linux | `/sys/kernel/mm/ksm/` | Disabled by default |
| lnstat | Linux | `/proc/net/stat/` | Disabled by default |
| loadavg | Darwin, Dragonfly, FreeBSD, Linux, NetBSD, OpenBSD, Solaris, AIX | `/proc/loadavg`, system calls | Enabled by default |
| logind | Linux | systemd-logind sessions | Disabled by default |
| mdadm | Linux | `/proc/mdstat` | Enabled by default |
| meminfo | Darwin, Dragonfly, FreeBSD, Linux, OpenBSD, NetBSD, AIX | `/proc/meminfo`, system calls | Enabled by default |
| meminfo_numa | Linux | `/sys/devices/system/node/node*/meminfo`, `/sys/devices/system/node/node*/numastat` | Disabled by default |
| mountstats | Linux | `/proc/self/mountstats` | Disabled by default |
| netclass | Linux | `/sys/class/net/` | Enabled by default |
| netdev | Darwin, Dragonfly, FreeBSD, Linux, OpenBSD, AIX | `/proc/net/dev`, network interface statistics | Enabled by default |
| netinterface | AIX | Network interface statistics | Enabled by default |
| netisr | FreeBSD | netisr statistics | Enabled by default |
| netstat | Linux, FreeBSD | `/proc/net/netstat` | Enabled by default |
| network_route | Linux | Routing table as metrics | Disabled by default |
| nfs | Linux | `/proc/net/rpc/nfs` | Enabled by default |
| nfsd | Linux | `/proc/net/rpc/nfsd` | Enabled by default |
| ntp | any | NTP daemon health | Deprecated |
| nvme | Linux | `/sys/class/nvme/` | Enabled by default |
| os | any | `/etc/os-release`, `/usr/lib/os-release` | Enabled by default |
| partition | AIX | Partition statistics | Enabled by default |
| pcidevice | Linux | PCI devices information | Disabled by default |
| perf | Linux | Linux perf events | Disabled by default |
| powersupplyclass | Linux, Darwin | `/sys/class/power_supply` | Enabled by default |
| pressure | Linux | `/proc/pressure/` (kernel 4.20+, CONFIG_PSI) | Enabled by default |
| processes | Linux | `/proc/` process statistics | Disabled by default |
| qdisc | Linux | Queuing discipline statistics | Disabled by default |
| rapl | Linux | `/sys/class/powercap` | Enabled by default |
| runit | any | runit service status | Deprecated |
| schedstat | Linux | `/proc/schedstat` | Enabled by default |
| selinux | Linux | SELinux statistics | Enabled by default |
| slabinfo | Linux | `/proc/slabinfo` | Disabled by default |
| sockstat | Linux | `/proc/net/sockstat` | Enabled by default |
| softirqs | Linux | `/proc/softirqs` | Disabled by default |
| softnet | Linux | `/proc/net/softnet_stat` | Enabled by default |
| stat | Linux | `/proc/stat` | Enabled by default |
| supervisord | any | supervisord service status | Deprecated |
| sysctl | Linux | `/proc/sys` | Disabled by default |
| systemd | Linux | systemd service and system status | Disabled by default |
| tapestats | Linux | `/sys/class/scsi_tape` | Enabled by default |
| tcpstat | Linux | `/proc/net/tcp`, `/proc/net/tcp6` | Disabled by default |
| textfile | any | Local disk text files | Enabled by default |
| thermal | Darwin | `pmset -g therm` | Enabled by default |
| thermal_zone | Linux | `/sys/class/thermal` | Enabled by default |
| time | any | Current system time | Enabled by default |
| timex | Linux | `adjtimex(2)` system call | Enabled by default |
| udp_queues | Linux | `/proc/net/udp`, `/proc/net/udp6` | Enabled by default |
| uname | Darwin, FreeBSD, Linux, OpenBSD | `uname` system call | Enabled by default |
| vmstat | Linux | `/proc/vmstat` | Enabled by default |
| watchdog | Linux | `/sys/class/watchdog` | Enabled by default |
| wifi | Linux | WiFi device and station statistics | Disabled by default |
| xfrm | Linux | `/proc/net/xfrm_stat` | Disabled by default |
| xfs | Linux | XFS runtime statistics (kernel 4.4+) | Enabled by default |
| zfs | FreeBSD, Linux, Solaris | ZFS performance statistics | Enabled by default |
| zoneinfo | Linux | NUMA memory zone metrics | Disabled by default |

## Notes

- **Enabled by default**: These collectors are active when node_exporter starts without additional configuration
- **Disabled by default**: These collectors must be explicitly enabled using `--collector.<name>` flags
- **Deprecated**: These collectors are deprecated and will be removed in future versions

## OS Abbreviations

- **Darwin**: macOS
- **Linux**: All Linux distributions
- **FreeBSD**: FreeBSD operating system
- **OpenBSD**: OpenBSD operating system
- **NetBSD**: NetBSD operating system
- **Dragonfly**: DragonFly BSD
- **Solaris**: Oracle Solaris
- **AIX**: IBM AIX
- **any**: Platform independent (available on all supported systems)

## Common Data Sources

- `/proc/*`: Linux procfs virtual filesystem containing kernel and process information
- `/sys/*`: Linux sysfs virtual filesystem containing hardware and system information
- **sysctl**: System control interface for kernel parameters
- **System calls**: Direct kernel interface calls (uname, adjtimex, etc.)
- **Hardware interfaces**: Direct hardware monitoring interfaces