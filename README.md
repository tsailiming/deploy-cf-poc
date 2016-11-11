Instructions for installing a canned demo
===

* Install latest CF 4.1.X . Give the instance at least 12GB of memory and 4 cores. 
* Run `ansible-playbook -i <ip>, -e rhsm_username=<username> -e rhsm_password=<password> -e rhsm_pool_id=<pool_id> site.yml`. 

Setup
====
* 1 Master tenant and 3 sub-tenant: Retail | Finance | Real Estate
* 1 Approval group
* 1 End user group
* Tenant quota
* Workers all reduced to 1. C&U turned off.
* Self-service catalog accessible by end user, Juan
* All providers/smtp username/password have been removed. :)
* Working catalogs for Azure/RHV/RHOSP/VMware
* Ansible tower integeration
* Drown SSL compliance with SSA
* Chargeback and other reports
* Include cloudbursting through Alerts -> Automation

User acccounts
====
* Admin: admin/smartvm
* End user: juan/password123
* Approval: albert/password123

Known issues/Limitations
====
* cloud-init doesn't work for Windows
* For VMware, open-vm-tools need to be installed in the intance and started to report IP address to ESXi -> vCenter -> CF

Todo
====
* Custom dashboard for end users
* Custom reports
* Incorporate custom build request (Generic type)
* Buttons
