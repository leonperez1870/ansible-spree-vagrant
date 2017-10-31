# Set your VM IP here
VMs = [
    [ "development", "10.1.1.11"],
    [ "production", "10.1.1.12"],
    [ "dbserver", "10.1.1.21"],
  ]

# VirtualBox Config with Ubuntu 16.04
Vagrant.configure(2) do |config|
  VMs.each { |vm|
    config.vm.define vm[0] do |box|
      box.vm.box = "geerlingguy/ubuntu1604"
      box.vm.network "private_network", ip: vm[1]
      box.vm.hostname = vm[0]
      box.vm.provider "virtualbox" do |vb|
        vb.memory = "512"
      end
    end
  }
end
