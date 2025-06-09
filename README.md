# Ansible-PCI

![Phorge logo](https://avatars.githubusercontent.com/u/187407936?s=200&v=4)

Ansible-PCI stores all the ansible configurations & file required to run the [Phorge Cloud Infrastructure](https://phorge.fr).

## Setup

requirements:

- [Ansible](https://ansible.com)

1. Install the requirements

```bash
ansible-galaxy collection install -r requirements.yml
```

2. Test environment

```bash
ansible -m ping all
```