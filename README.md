# firstrun

## General info
Simple ansible play to create user and change ssh port for future ansible connections.
Configuration options are stored in ansible vault.
Passwords for root and new user are mandatory. Play may add new user to sudoers.d.
No additional ssh hardening, changing port works only for default ssh configuration file.
Tested on Buster only.

## How to use
Few options may be used, thorough variables in host/group vaults.
Create vault file with variables:
- vault_ansible_user_name
- vault_ansible_user_uid_nr       (optional)
- vault_ansible_user_pubkey_path
- vault_ansible_user_pass
- vault_su_or_sudo                (su or sudo)
- vault_root_pass
- vault_ssh_port_new              (optional)

