# create-launch-configuration

Create launch configuration

# Requirements

The role uses the EC2 module, the boto package is required.

# Role Variables

* `lc_name`                : Name of the launch configuration
* `lc_ami`                 : AMI ID for the launch configuration
* `lc_security_groups`     : Security group IDs for the launch configuration
* `lc_user_data`           : User data for the launch configuration
* `instance_monitoring`    : [yes|no] to monitor
* `region`                 : Region to launch the ec2 instance to create the new AMI
* `keypair`                : SSH keypair to access
* `instance_type`          : AWS instance type
* `instance_profile_name ` : The name or the Amazon Resource Name (ARN) of the instance profile associated with the IAM role for the instances

# Example playbook

```yaml
- hosts: localhost
  connection: local
  gather_facts: no
  roles:
    - create-launch-configuration
```

# License

GPLv2

# Author Information
jamatute (jamatute@paradigma)
