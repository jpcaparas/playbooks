# JP's Playbooks

This repository contains Ansible playbooks to provision different types of machines:

- Common: Base packages installed on all machines
- Server: Packages for servers, imports common playbook 
- Workstation: Packages for workstations, imports server and common playbooks
- Friend: Packages for friend's machines, imports common playbook

## Running Playbooks

1. Install Ansible on your local machine
1. Clone this repository 
1. Update the `inventory` file with the hosts to provision
1. Run the desired playbook

## Supported Platforms

The playbooks are tested on:
- macOS 
- Fedora/RHEL
- Debian/Ubuntu

Some packages are OS specific and will only be installed if supported on the target platform.
