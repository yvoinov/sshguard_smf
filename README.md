# Solaris SSHGuard SMF
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://github.com/yvoinov/sshguard_smf/blob/master/LICENSE)

This set of scripts is designed to install and remove the SMF service for SSHGuard on Sun Solaris 10 and above.

All the necessary prerequisites required to start the SSHGuard service, according to the configuration guide (excluding the configuration of the SSHGuard itself) are performed during the installation of the service, removing the SMF service removes all scripts and unregisters the SSHGuard service and stops it.

Follow these steps to enable sshguard SMF:

1. Install SSHGuard and all required libraries if not already installed.

2. Put SSHGuard config to it's place (usually /usr/local/etc).

3. Run the sshguard_smf_inst.sh script, which will perform all the necessary prerequisites and post-installation steps and install the SSHGuard SMF service.

3. Run `svcadm enable sshguard` command to enable and start the SSHGuard service.

To deactivate and remove the SSHGuard SMF service, follow these steps:

1. Run the sshguard_smf_rmv.sh script. The script stops all running SSHGuard processes, unregisters the SMF service, completely removes the SSHGuard SMF and rolls back the operations performed earlier when the service was activated.

Note: Removing the SSHGuard SMF service does not remove the installed SSHGuard software.

