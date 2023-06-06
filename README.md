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

# Post Tasks

## synology ssh access using keys

During the synology role, a key pair will be created. The public will need to be copied to the Synology station for the targeted Synology account.

## systemd on user level

No user level systemd services can be enabled with an actual login to the account. Because of this, enabling for example the datasync service will not work and you receive the error message:

```bash
Failed to connect to bus: No medium found
```

Log in to the targeted account and run it manually.
