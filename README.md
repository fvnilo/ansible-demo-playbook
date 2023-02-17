# ansible-demo-playbook

A very simple Ansible playbook example to illustrate various concepts.

This playbook simply installs nginx in an EC2 that we assume is running an Amazon Linux 2 AMI

## Getting Started

### Locally

Because there is a [`local.yml`](/local.yml) file in this repository, you can pull this repository and make it run automatically with this command:

```
ansible-pull -U URL_OF_THE_PLAYBOOK
```

### Remotely

You can also **push** the configuration remotely by running this command:

```
ansible-playbook -i aws_ec2.yml site.yml
```

### The Inventory

The inventory is using the `aws_ec2` Ansible plugin. You need to have one or more instance with the Name tag as `webserver-demo`.

[Click here](https://docs.ansible.com/ansible/latest/plugins/inventory.html#inventory-plugins) for more info.
