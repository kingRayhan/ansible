## Ansible Playbooks

### Ping all hosts

```bash
ansible -i inventory.yml all -m ping
```

# Caddy

```
# For full installation with user setup
ansible-playbook -i inventory.yml caddy.yml --tags "fresh_install"

# For installation and configuration
ansible-playbook -i inventory.yml caddy.yml --tags "install"

# To just update configuration
ansible-playbook -i inventory.yml caddy.yml --tags "config"

# To stop the service
ansible-playbook -i inventory.yml caddy.yml --tags "service_stop"

# For complete uninstallation
ansible-playbook -i inventory.yml caddy.yml --tags "uninstall"
```

# Docker

```
# For basic installation
ansible-playbook -i inventory.yml playbook.yml --tags "install"

# For full installation with user setup
ansible-playbook -i inventory.yml playbook.yml --tags "fresh_install"

# Just to stop services
ansible-playbook -i inventory.yml playbook.yml --tags "service_stop"

# For complete uninstallation (includes stopping services)
ansible-playbook -i inventory.yml playbook.yml --tags "uninstall"
```
