# Ansible Wiriguard 

This role work with:
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)

## How it works:

Setup new server:

Before start script, you should add ip servers to inventory

```bash
ansible-playbook wg_srv_conf.yml -i inventory -e "hosts=all"
```

Add new user config:

```bash
ansible-playbook wg_add_usr.yml -i inventory -e "hosts=all uname=*** usr_ip=***"
```

Where you need write user name and ip instead of ***

The new configuration will be located in the `/etc/wireguard/*uname*/`
