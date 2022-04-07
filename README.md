# VM PROVISIONING WITH VAGRANT

## Get started with vagrant

#### [How to install vagrant ?](https://linuxize.com/post/how-to-install-vagrant-on-ubuntu-20-04/)
* ***install vagrant***
    > *Vagrant need a virtualization software where vm will be create. I'm using virtualbox*
```
sudo apt update
sudo apt install -y virtualbox vagrant
```

#### [How to use vagrant ?](https://www.vagrantup.com/docs)
* ***vagrant init*** cmd
    > *create a vagrant file from vagrant box from Vagrant Cloud*
```
vagrant init $VagrantBoxName 
```
* ***vagrant up*** cmd
    > *run the vagantfile create above to deploy and start a VM*
```
vagrant up
```

#### [Repository Directory Tree](https://gitlab.com/i3017/vm-provisioning-with-vagrant.git)
* folder ***vm-all-in-one***
    > *contain vagrantfile to create and start VM for cluster kubernetes and devops host*
* folder ***vm-cluster-kubernetes***
    > *contain vagrantfile to create and start VM for cluster kubernetes*
* folder ***vm-devops-host***
    > *contain vagrantfile to create and start VM fordevops host*
* folder ***ansible-playbook***
    > *contain playbook to automate configuration of VM deplpoyed*
