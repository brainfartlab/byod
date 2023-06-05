# BYOD: Bring Your Own Device

Ansible playbooks for our BYOD setup.

## Execution

```bash
ansible-playbook playbooks/bangalore.yml \
    --become \
    --become-user <user> \
    --ask-become-pass \
    --vault-password-file <vault-pass-file>
```
