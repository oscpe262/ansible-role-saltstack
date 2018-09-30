# Ansible role 'ansible-role-saltstack'

An Ansible role for setting up SaltStack on Fedora.
Now, of course you might think "why the heck would I want to use Ansible to install SaltStack"? Well, because Ansible is awesome.
I decided to broaden my skillset, and why not try SaltStack? Does this mean either one is better than the other?
No, they are to some extent overlapping in functionality, and both have upsides compared to the other. However, that is outside
the scope of a simple role README.

Due to compat issues with firewalld-module, this role won't bother with firewall configs. Please open ports 4505-4506 manually if
needed.

## Requirements
Fedora (28 tested)

## Role Variables
| Variable		| Default		| Comments (type) |
| salt_master_node | absent | Whether to install the SaltStack Master package `(absent|present)` |
| salt_master_fqdn | localhost | IP or fqdn for the master node |
| master_pub | | Output found by running `salt-key -F master` on the master node. If undefined, it won't be used (recommended first run) |
| :---			| :---			| :---		  |


## Dependencies

## Example Playbook
```Yaml
- hosts: foo
  roles:
    - role: ansible-role-saltstack
```

## Testing


## License

BSD

## Contributors

Issues, feature requests, ideas, suggestions, etc. are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Please create a topic branch for your proposed changes, it's the easiest way to merge back into the project.

- [Oscar Petersson](https://github.com/oscpe262/) (Maintainer)
