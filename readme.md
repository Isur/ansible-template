# VPS setup

This ansible playbook will setup server.

- install docker;
- create user;
    - setup username in `playbook.yml`
- setup firewall;
    - allowed only: 22, 80, 443
- setup zsh with plugins;
- install lazydocker and other utils;
- setup ssh:
    - `./roles/user/files/id_rsa.pub` - change key for your public key;

# Pre

Before run setup `inventory.yml`.

To install required collections:

```bash
ansible-galaxy install -r collections.yml
```
# Run

To run playbook:

```bash
ansible-playbook playbook.yml -i inventory.yml -K --vault-password-file=$PATH_TO_FILE
```
