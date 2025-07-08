============================================================
sshguard SMF Installation & Remove (C) 2007-2025 Yuri Voinov
============================================================

***  WARNING!  The  package  is configured by default to run
sshguard installed in /use/local!

This  set  of  scripts is designed to install and remove the
SMF service for sshguard on Sun Solaris 10.

To enable sshguard SMF, follow these steps:
-------------------------------------------

1. Install sshguard if you haven't already.

2. Configure sshguard.

3.  If  necessary, edit the BASE_DIR parameter (variable) in
the  init.sshguard script so that it points to the directory
where sshguard is actually installed.

4.  Run  the sshguard_smf_inst.sh script, which will perform
all  necessary  prerequisites  and post-installation actions
and install the sshguard SMF service.

5.  Run  the  svcadm  enable  sshguard command to enable and
start the sshguard service.

To  disable  and  remove  sshguard SMF service, follow these
steps:
------------------------------------------------------------

1.  Run the sshguard_smf_rmv.sh script. The script stops all
running  sshguard  processes,  unregisters  the SMF service,
completely   removes   sshguard   SMF  and  rolls  back  the
operations   previously   performed  when  the  service  was
activated.

***  Note: Removing the sshguard SMF service does not remove
the installed SSHGuard software.

The archive contains:

init.sshguard           - sshguard SMF control method
sshguard.xml            - sshguard SMF service manifest
readme_ru.txt           - This file (Russian)
readme_en.txt           - This file (English)
sshguard_smf_inst.sh    - SSHguard SMF Installation Script
sshguard_smf_rmv.sh     - SSHGuard SMF Removal Script

============================================================
sshguard SMF Installation & Remove (C) 2007-2025 Yuri Voinov
============================================================