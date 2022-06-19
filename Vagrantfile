Vagrant.configure("2") do |config|

  config.vm.provider "virtualbox" do |vbox|
    vbox.memory = 1024
    vbox.cpus = 1
  end

  config.vm.define "zabbix-server" do |zserver|
    zserver.vm.box = "centos/7"
    zserver.vm.disk :disk, size: "100GB", primary: true
    zserver.vm.network "private_network", ip: "192.168.56.10"
  end

  config.vm.define "zabbix-proxy" do |zproxy|
    zproxy.vm.box = "centos/7"
    zproxy.vm.disk :disk, size: "30GB", primary: true
    zproxy.vm.network "private_network", ip: "192.168.56.20"
  end

  config.vm.define "zabbix-agent" do |zagent|
    zagent.vm.box = "centos/7"
    zagent.vm.disk :disk, size: "20GB", primary: true
    zagent.vm.network "private_network", ip: "192.168.56.30"
  end

end
