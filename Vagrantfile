Vagrant.configure("2") do |config|
  config.vm.box_download_insecure=true
  config.vm.box = "bento/ubuntu-22.04"
  config.vm.box_check_update = false

  config.vm.provider :virtualbox do |v|
    v.customize ["modifyvm", :id, "--memory", 3072]
  end

  config.vm.define "master" do |master|
    master.vm.box_check_update = false
    master.vm.hostname = "master"
    master.vm.network :private_network, ip: "192.168.56.100"
  end

  config.vm.define "node1" do |node1|
    node1.vm.box_check_update = false
    node1.vm.hostname = 'node1'
    node1.vm.network :private_network, ip: "192.168.56.101"
  end

  config.vm.define "node2" do |node2|
    node2.vm.box_check_update = false
    node2.vm.hostname = 'node2'
    node2.vm.network :private_network, ip: "192.168.56.102"
  end
end
  
  
