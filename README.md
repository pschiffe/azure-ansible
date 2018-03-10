# Ansible for Azure and OpenShift

Ansible roles and playbooks for Azure and OpenShift.

## Requirements

### Ansible

```
sudo dnf install ansible
```

### Azure SDK for Python

There is a `python2-azure-sdk` rpm package, but it contains an old version of Azure SDK, so it has to be installed from pip:

```
sudo pip2 install 'azure>=2.0.0,<3'
```

### Credentials

Create a `~/.azure/credentials` file according to the http://docs.ansible.com/ansible/latest/guide_azure.html#storing-in-a-file

## Configuration

Create a `group_vars/all/99_custom.yml` file with defined variables: `azure_ci_resource_group`, `azure_ci_ssh_privkey_path` and `azure_ci_ssh_pubkey`.

## Example usage

```
ansible-playbook create_simple_infra.yml
```
