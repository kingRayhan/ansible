## Ansible Playbooks

### Ping all hosts

```bash
ansible -i inventory.cfg all -m ping
```

### Caddy

Install Caddy and configure reverse proxy for example.com and api.example.com

```bash
ansible-playbook -i inventory.cfg caddy.yml --tags fresh_install
```

Stop and disable Caddy service

```bash
ansible-playbook -i inventory.cfg caddy.yml --tags stop_service
```

Configure reverse proxy for example.com

```bash
ansible-playbook -i inventory.cfg caddy.yml --tags configure_reverse_proxy
```

### Install Docker

```bash
ansible-playbook -i inventory.cfg docker.yml
```
