## Ansible playbook to create new VM on DevOps lab system

#### Require

Ansible >= 2.5 

#### How to use

Configuration VM parameters in `./group_vars/all` 

Select Physical Server to host VM in `./hosts`

Then run following command: 

```
ansible-playbook -i hosts sites.yml
```

### Info

- Box : `centos/7`
- User/pass : `vagrant/vagrant`
