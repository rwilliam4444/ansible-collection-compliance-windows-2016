# Role Name:
- ansible-collection-compliance-windows-2016

# Description:
This playbook is a collection of windows 2016 CIS compliance roles. Group
Policy settings may override these local settings. When the role's "remediate"
variable is set to "YES", the role will try to remediate the server's setting(s)
according to the CIS standards.  Each role has a defaults/main.yml file which
can be used to disable specific CIS items (i.e."execute_<cis task #>") from
executing. The default value in the defaults/main.yml for these CIS item
variables (i.e. "execute_<cis task #>") is set to "YES". The value "YES" means
that the CIS item will execute at run time. Set the value to "NO" if you want to
skip this CIS item in question from executing.

# Requirements:
Windows Ansible related pre-requisites

# Default roles in this collection playbook:
__role_name__ | ansible-role-compliance-windows-advance-audit-logging-2016.
__role_name__ | ansible-role-compliance-windows-control-panel-policy-2016.
__role_name__ | ansible-role-compliance-windows-firewall-policy-2016.
__role_name__ | ansible-role-compliance-windows-laps-policy-2016.
__role_name__ | ansible-role-compliance-windows-mss-policy-2016.
__role_name__ | ansible-role-compliance-windows-network-policy-2016.
__role_name__ | ansible-role-compliance-windows-password-policy-2016.
__role_name__ | ansible-role-compliance-windows-scm-policy-2016.
__role_name__ | ansible-role-compliance-windows-security-options-policy-2016.
__role_name__ | ansible-role-compliance-windows-system-policy-2016.
__role_name__ | ansible-role-compliance-windows-user-rights-policy-2016.


# Example Playbook:
---
 - name: ansible-collection-compliance-windows-2016.
   hosts: "{{var_hosts}}"

   roles:
   - ansible-role-compliance-windows-advance-audit-logging-2016
   - ansible-role-compliance-windows-control-panel-policy-2016
   - ansible-role-compliance-windows-firewall-policy-2016
   - ansible-role-compliance-windows-laps-policy-2016
   - ansible-role-compliance-windows-mss-policy-2016
   - ansible-role-compliance-windows-network-policy-2016
   - ansible-role-compliance-windows-password-policy-2016
   - ansible-role-compliance-windows-scm-policy-2016
   - ansible-role-compliance-windows-security-options-policy-2016
   - ansible-role-compliance-windows-system-policy-2016
   - ansible-role-compliance-windows-user-rights-policy-2016
   - ansible-role-compliance-windows-windows-components-policy-2016


# Author Information:
Richard M. Williams (williamsitv@yahoo.com)
