# deploy_snmp_ansible

This playbook installs Net-SNMP on RHEL/CentOS servers and creates a SNMPv3 user. 

Complete action list:
1. Install Net-SNMP
2. Create SNMPv3 user
3. Open SNMP ports on firewalld
4. Starts and enables snmpd to start on boot
5. Restart firewalld

Optionally, if you are using LibreNMS, you can uncomment the #get-distro-file line and the playbook will retrieve and apply permissions to the distro script. The distro script is used by the SNMP manager to detect which OS/distribution is running.