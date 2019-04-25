# base_config_ansible
Loads blank RHEL/CentOS servers with basic start up packages and configurations. The configuration file for Rsyslog, Chrony(NTP), and Net-SNMP are the default files that are pulled from the yum repository. Edit as needed.

This script installs:
- nano 
- open-vm-tools
- bind-utils
- epel-release
- firewalld
- libselinux-python
- cockpit
- setroubleshoot-server

This script installs and configures:
- chrony
- rsyslog
- net-snmp

By default, the script is set to create a SNMPv3 user. Edit the credentials. 
Edit the Rsyslog and NTP configuration files to point to your servers.

Optionally, if you are using LibreNMS, you can uncomment the #get-distro-file line and the playbook will retrieve and apply permissions to the distro script. The distro script is used by the SNMP manager to more accurately detect which OS/distribution is running.