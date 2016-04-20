### Usage

###### To run usage playbooks for all services:
```shell
openstack-ansible setup-usage.yml
```

###### To run usage playbooks for a specific service:
```shell
openstack-ansible os-<service>-usage.yml
```

### Configuration
```ini
[defaults]
# Additional plugins
# Need to know location of openstack ansible plugins
lookup_plugins = <path to openstack-ansible>/playbooks/plugins/lookups
filter_plugins = <path to openstack-ansible>/playbooks/plugins/filters
action_plugins = <path to openstack-ansible>/playbooks/plugins/actions

gathering = smart

# Fact caching
fact_caching = jsonfile
fact_caching_connection = /etc/openstack_deploy/ansible_facts
fact_caching_timeout = 86400

# Need to know location of openstack ansible dynamic inventory
inventory = <path to openstack-ansible>/playbooks/inventory
host_key_checking = False

# Set color options
nocolor = 0

# SSH timeout
timeout = 120

[ssh_connection]
pipelining = True
```
