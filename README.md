# addon-openstack
Cloud bursting driver to integrate OpenStack hosts into OpenNebula cloud

# Compatibility
This add-on is compatible with OpenNebula 4.14.2

# Local Vagrant setup
To have actual version of OpenNebula for tests and experiments, there is a Vagrant+Ansible setup in ./vagrant folder.

## Prerequisites
Oracle VirtualBox (tested with 5.0.14)
Vagrant (tested with 1.8.1)
Vagrant-vbguest plugin (tested with 0.11.0)
Ansible (tested with 2.0.0.2)

## Installation Steps
```bash
cd ./vagrant
cp my_os_credentials.example.yml.j2 my_os_credentials.yml.j2
# edit your OpenStack credentials in my_os_credentials.yml.j2 (it will stay on your machine and will never be committed to the Git) 
vagrant up
# if you get "Timed out while waiting for the machine to boot. This means that" try Ctrl+C and continue with the next Steps
# alternative: login through Virtualbox "show" and start "dnclient" manually
vagrant provision
```
now you can visit [Sunstone](http://192.168.35.80:9869) for user interface and be able to import wild-VMs from OpenStack


# Useful Links
- [How to Develop a New Driver to Interact with an External Cloud Provider](http://community.opennebula.org/cloud_provider_driver)
- [Cloud Bursting Driver](http://docs.opennebula.org/4.14/integration/infrastructure_integration/devel-cloudbursting.html)
- [ONE Amazon EC2 Driver](https://github.com/OpenNebula/docs/blob/master/source/advanced_administration/cloud_bursting/ec2g.rst)

# Special Thanks
to OpenNebula team for such a great project!
