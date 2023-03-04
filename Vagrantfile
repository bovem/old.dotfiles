Vagrant.configure("2") do |config|
  # config.vm.box = "fedora/37-cloud-base"
  config.vm.box = "ubuntu/focal64"

  config.vm.network "private_network", ip: "192.168.56.10"
  # config.vm.synced_folder ".", "/home/vagrant/data"
  config.vm.hostname = "DevEnv"
  config.vm.define "DevEnv"
  config.vm.provider "virtualbox" do |vb|
      vb.name = "DevEnv"
      vb.customize ["modifyvm", :id, "--nested-hw-virt", "on"]
      vb.cpus = 4
      vb.memory = "4196"
  end
end
