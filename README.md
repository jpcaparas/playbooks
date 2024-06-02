# JP's Playbooks

This repository contains Ansible playbooks to provision different types of Ubuntu machines:

- Common: Base packages installed on all machines
- Server: Packages for servers, imports common playbook 
- Workstation: Packages for workstations, imports server and common playbooks
- Friend: Packages for friend's machines, imports common playbook

## Running Playbooks

1. [Install Ansible v2.x](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) on your local machine
1. Clone this repository 
1. Run: 
   - Common packages: `ansible-playbook playbook.yml -vvv`
   - Server packages: `ansible-playbook playbook.yml -vvv --tags=server`
   - Workstation packages: `ansible-playbook playbook.yml -vvv --tags=workstation`
   - Combination server + workstation packages: `ansible-playbook playbook.yml -vvv --tags=server,workstation`
   - Friend packages: `ansible-playbook playbook.yml -vvv --tags=friend`

Some packages are OS-specific and will only be installed if supported on the target platform.
