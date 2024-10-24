# Debian-MotD
Custom MotD for Debian Systems

# System Information Scripts

This repository contains several shell scripts designed to display system information, check for updates, and show relevant system messages.

## Files Overview

1. **00-header**: 
   This script provides a welcome message, displays basic system details such as the distribution name, version, kernel, and architecture, and includes links to official Debian resources. The script outputs system information at login.

   Key details included:
   - Distribution: Debian
   - Version and codename
   - Kernel version and architecture
   - Links to documentation, support, and bug reporting for Debian

2. **10-sysinfo**:
   This script displays key system metrics such as CPU load, root partition usage, memory usage, swap usage, and CPU temperature (if available). It also provides network information, including both IPv4 and IPv6 addresses, the number of processes running, and the number of users logged in.

   Information captured:
   - System load
   - Root filesystem usage
   - Memory and swap usage
   - CPU temperature (if available)
   - Number of processes and users logged in
   - IPv4 and IPv6 addresses for the system
   
3. **90-updates**:
   This script checks for available system updates, including security updates. It counts the number of upgradable packages and shows the number of standard security updates, if any, that can be applied immediately.

   Features:
   - Count of available updates
   - Count of security updates
   - Command hint for listing available updates (`apt list --upgradable`)

## Usage

To use these scripts, clone the repository and ensure that the scripts are executable. You can place them in `/etc/update-motd.d/` to have the messages displayed upon login in a Debian-based system.

```bash
chmod +x 00-header 10-sysinfo 90-updates


