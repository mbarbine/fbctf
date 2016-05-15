# -*- mode: ruby -*-
# vi: set ft=ruby :
config.vm.provider :digital_ocean do |provider, override|

    override.vm.box = 'digital_ocean'
    override.vm.box_url = "https://github.com/devopsgroup-io/vagrant-digitalocean/raw/master/box/digital_ocean.box"
   



    #
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "10.10.10.5"
  config.vm.hostname = "facebookCTF-Dev"
  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"
  config.vm.provision "shell", path: "extra/provision.sh", privileged: false
  provider.ssh_key_name = 'Vagrant'
  provider.token = '29a4eb304dd0d2967ef1c41886ca98733f5bd62b1bf5afb45dda4872b1585dbf'
  provider.image = '17216123'
  provider.region = 'nyc2'
  provider.size = '2gb'
  provider.disk = '40gb'
 end
end
