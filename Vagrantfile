Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

  config.vm.define "mysql" do |db|
    db.vm.network "private_network", ip: "10.55.80.20"
    db.vm.network "forwarded_port", guest: 3306, host: 3306
    db.vm.provision "shell", path: "bootstrap.sh"
  end
end
