VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.private_key_path = "~/.ssh/id_rsa"
  config.vm.box = "ubuntu/xenial64"  
  config.vm.provider "virtualbox" do |vb|
     vb.customize ["modifyvm", :id, "--memory", "1024"]
  end

  config.vm.define "master" do |master|    
    master.vm.network "private_network", ip: "192.168.99.101"
  end

  config.vm.define "slave" do |slave|
    slave.vm.network "private_network", ip: "192.168.99.102"
  end

end
