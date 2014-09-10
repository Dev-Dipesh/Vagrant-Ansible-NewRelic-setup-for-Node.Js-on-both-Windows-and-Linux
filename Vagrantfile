# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "precise32"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  config.vm.network :forwarded_port, guest: 8080, host: 8080
  config.vm.network :forwarded_port, guest: 80, host: 3001
  # config.vm.network :forwarded_port, guest: 7777, host: 7777

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", type: "dhcp"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network :public_network

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  config.vm.synced_folder "./", "/home/vagrant/source"

  # vagrant plugin install vagrant-hostsupdater
  # vagrant plugin uninstall vagrant-hostsupdater

  # Use a prebuilt hostname, if you have vagrant-hostupdater, it will
  # Update your host machines etc/host file with the private_network ip
  # above.  This way, you never have to edit your host file, just use:
  config.vm.hostname = "local.friendzy.com"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1500
    v.cpus = 2
  end

  # Use rbconfig to determine if we're on a windows host or not.
  require 'rbconfig'
  is_windows = (RbConfig::CONFIG['host_os'] =~ /mswin|mingw|cygwin/)
  if is_windows
    # Provisioning configuration for shell script.
    config.vm.provision "shell" do |sh|
      sh.path = "ansible/windows.sh"
      sh.args = "ansible/playbook.yml ansible/hosts/hosts.local"
    end
  else
    # Provisioning configuration for Ansible (for Mac/Linux hosts).
    config.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/playbook.yml"
      ansible.inventory_path = "ansible/hosts/hosts.local"
      # ansible.inventory_file = "ansible/hosts/hosts.local"
    end
  end
end
