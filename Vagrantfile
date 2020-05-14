Vagrant.configure("2") do |config|
  config.vm.define "slave1" do |slave1|
    slave1.vm.box = "bento/ubuntu-18.04"
    slave1.vm.hostname = 'slave1'
    slave1.vm.box_url = "bento/ubuntu-18.04"

    slave1.vm.network :private_network, ip: "192.168.56.101"

    slave1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "slave1"]
    end
  end

  config.vm.define "slave2" do |slave2|
    slave2.vm.box = "bento/ubuntu-18.04"
    slave2.vm.hostname = 'slave2'
    slave2.vm.box_url = "bento/ubuntu-18.04"

    slave2.vm.network :private_network, ip: "192.168.56.102"

    slave2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "slave2"]
    end
  end
end
