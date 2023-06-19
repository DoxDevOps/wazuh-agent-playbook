# wazuh-agent-playbook

This README provides instructions on how to install and start the Wazuh agent on a group of webservers. The provided Ansible playbook automates the installation process by downloading the Wazuh agent deb file, installing it, and configuring it to connect to a Wazuh manager.

## Prerequisites

- Ansible installed on the control machine.
- Appropriate SSH access and credentials to the webservers.
- Internet connectivity on the webservers to download the Wazuh agent deb file.

## Instructions

1. Modify the Ansible playbook according to your environment requirements. Open the playbook file  and make the following changes if necessary:

   - Update the `hosts` value to specify the target group of webservers.
   - Modify the `WAZUH_MANAGER` and `WAZUH_AGENT_GROUP` values under the "Install Wazuh agent" task to match your Wazuh manager's IP address and the desired agent group name.

2. Execute the playbook by running the following command in the terminal:

   ```
   ansible-playbook install_agent.yml
   ```

   This command will initiate the installation process and start the Wazuh agent on the specified webservers.

3. Monitor the playbook execution for any errors or warnings. Once the playbook completes without any issues, the Wazuh agent should be installed and running on the webservers.

## Additional Notes

- Ensure that the Wazuh manager is accessible from the webservers and configured to accept agent connections from the specified agent group.

