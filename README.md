# Intel User Lab Infrastructure Deployment

The Intel User Lab is an environment that does not connect to the main Intel infrastructure. Due to this, the standard services of DNS and DHCP are not available for this lab. We built this Ansible playbook to provide the missing services.

## How To Execute This Playbook

This playbook is intended to be executed from the Primary server within the lab. Since the primary server is a fully deployed Fedora server with a static ip address, a defined user account, and has updated its `dnf` library, the only requirement to execute this playbook is the installation of Ansible on the primary server.

To execute, run the following command from the root of this git repo:

``` sh
ansible-playbook -i inventory/hosts.ini setup_lab.yml
```
