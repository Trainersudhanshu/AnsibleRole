Role Name
=========

This role will launch aws ec2 instance and will also configure the inventory dynamicly, Then it will further setup the webserver in that target node

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

This role uses two variable files, **main.yml* and **aws_credential.ynl*, In **main.yml** we have defined all the normal variable which playbook will be using. and in **aws_credential.yml** two variable are defined with name - **aws_access_key and aws_secret_key**, So before using this playbook, create a file with name aws_credential.yml inside /roles/rolename/vars/, you can delete my aws_credential.yml file(as it is locked via my vault password), So you create this file, and give your credentials in respective above variable and then lock this file again with your ansible-vault(use command - ansible-vault create --vault-password-file secret.txt aws_credential.yml)

Dependencies
------------

This role uses the community.aws collection, So before using this role, you should have this collection installed, Run the command - **ansible-galaxy collection install community.aws**

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: rolename

License
-------

BSD

Author Information
------------------

This Role is created by **Sudhanshu Pandey**, Check further about him here - https://www.linkedin.com/in/sudhanshu--pandey/
