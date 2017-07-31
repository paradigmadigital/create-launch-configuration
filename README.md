# create-launch-configuration

Create launch configuration

# Requirements

The role uses the EC2 module, the boto package is required.

# Role Variables

* `lc.name`                   : Name of the launch configuration
* `lc.ami_id`                 : AMI ID for the launch configuration
* `lc.security_groups`        : Security group IDs for the launch configuration
* `lc.user_data`              : User data for the launch configuration
* `lc.instance_monitoring`    : [yes|no] to monitor
* `lc.region`                 : Region to launch the ec2 instance to create the new AMI
* `lc.keypair`                : SSH keypair to access
* `lc.instance_type`          : AWS instance type
* `lc.instance_profile_name`  : The name or the Amazon Resource Name (ARN) of the instance profile associated with the IAM role for the instances
* `lc.assign_public_ip`       : Used for Auto Scaling groups that launch instances into an Amazon Virtual Private Cloud. Specifies whether to assign a public IP address to each instance launched in a Amazon VPC.  [Default: (null)]

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
