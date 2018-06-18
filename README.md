# host_preparation

## Description:

Subscribe a system to Red Hat, directly 



## Behaviour:

**Feature:** Subscribe a system to Red Hat
- **Given** a VM of capable size and power is available
- **Given** the connection details to the VM are known
- **When** A new RHEL-system has been installed
- **Then** Change the RHEL-system hostname according to private dns
- **Then** register it to Red Hat
- **Then** attach subscriptions
- **Then** disable all other repositories
- **Then** enable base repository
- **Then** reboot system
- **Then** installing docker
- **Then** setting up docker storage

## Configuration:

Common variables used by this role:

| Variable  | Description  | Example  | 
|---|---|---|
| **redhat_activationkey** | Red Hat Activation Key | |
| **redhat_organization_id** | Red Hat Organization ID |  |
| **redhat_pool_ids** | Red Hat Subscription Pool IDs |  |

## Usage:

How to invoke the role from a playbook:

```yaml
- name: Subscribe to Red Hat
  include_role:
    name: host_preparation
  vars:
    redhat_activationkey: myuser
    redhat_organization_id: myuser
```

Note: add common variables to the `vars` list as required.
