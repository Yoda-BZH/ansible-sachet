# Ansible Role: sachet

Provision and manage [sachet](https://github.com/messagebird/sachet) - plugin to send AlertManager's Alerts through SMS Provider

## Requirements

- Ansible >= 2.5

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `sachet_version` | latest | Sachet package version |
| `sachet_instance` | {{ ansible_fqdn \| default(ansible_host) \| default(inventory_hostname) }} | Sachet instance name |
| `sachet_address` | 127.0.0.1 | Address on which sachet listens |
| `sachet_port` | 9876 | port on which sachet listens |
| `sachet_repository ` | github.com/messagebird/sachet/cmd/sachet | github link to the source code |

Mandatory Variables:

| Name                  |  Description                        |
| --------------------- | -----------------------------------|
| `freemobile_username` | FreeMobile Username for API Usage |
| `freemobile_password` | FreeMobile Password for API Usage |

## Notes

This role works only with the [FreeMobile]('https://mobile.free.fr/') Carrier Provider.  
It's Debian-based Only.  

Issues & PR are welcome for any improvement.  

This is heavily inspired by [CloudAlchemy]('https://github.com/cloudalchemy/')