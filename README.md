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

## Deploy main k3s cluster

requirements:

- [k3s group vars](./inventories/production/group_vars/k3s_cluster.yml)
- [hosts file](./inventories/production/hosts)
- [collections](#setup)

1. Deploy k3s cluster:

```bash
ansible-playbook collections/ansible_collections/techno_tim/k3s_ansible/site.yml
```

2. Get kubeconfig:

```bash
cat collections/ansible_collections/techno_tim/k3s_ansible/kubeconfig > ~/.kube/config
```