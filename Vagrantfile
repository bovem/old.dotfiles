Vagrant.configure("2") do |config|
  config.vm.box = "fedora/35-cloud-base"

  config.vm.network "private_network", ip: "192.168.56.10"

  config.vm.hostname = "devenv"
  config.vm.define "devenv"
  config.vm.provider "virtualbox" do |vb|
      vb.name = "devenv"
      vb.customize ["modifyvm", :id, "--nested-hw-virt", "on"]
      vb.cpus = 4
      vb.memory = "4196"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "setup_playbook.yaml"
  end
end
