# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  #-------------------------------------------------------------------------------------------------------------------
  config.vm.define "master1" do |master|
    master.vm.box = "centos/7"
    master.vm.hostname = "master"
    master.vm.network :private_network, ip: "192.168.40.2"
    master.vm.provider "virtualbox" do |v|
      v.memory = 2048
   end
   $COMMANDS = <<-"BLOCK"
   sudo sed -i "s/PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config;
   sudo systemctl restart sshd;
   sudo yum -y install epel-release;
   sudo yum -y install ansible;
   BLOCK
   config.vm.provision "shell", inline: $COMMANDS
  end
  #-------------------------------------------------------------------------------------------------------------------
  config.vm.define "slve" do |slave|
    slave.vm.box = "centos/7"
    slave.vm.hostname = "slave"
    slave.vm.network :private_network, ip: "192.168.40.3"
    slave.vm.provider "virtualbox" do |v|
      v.memory = 4096
  end
  $COMMANDS = <<-"BLOCK"
  sudo sed -i "s/PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config;
  sudo systemctl restart sshd;
  BLOCK
  config.vm.provision "shell", inline: $COMMANDS
end
  #-------------------------------------------------------------------------------------------------------------------
config.vm.define "slve2" do |slave|
  slave.vm.box = "centos/7"
  slave.vm.hostname = "slave2"
  slave.vm.network :private_network, ip: "192.168.40.4"
  slave.vm.provider "virtualbox" do |v|
    v.memory = 2048
end
$COMMANDS = <<-"BLOCK"
sudo sed -i "s/PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config;
sudo systemctl restart sshd;
BLOCK
config.vm.provision "shell", inline: $COMMANDS
end
  #-------------------------------------------------------------------------------------------------------------------
config.vm.define "slve3" do |slave|
  slave.vm.box = "centos/7"
  slave.vm.hostname = "slave3"
  slave.vm.network :private_network, ip: "192.168.40.8"
  slave.vm.provider "virtualbox" do |v|
    v.memory = 2048
end
$COMMANDS = <<-"BLOCK"
sudo sed -i "s/PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config;
sudo systemctl restart sshd;
BLOCK
config.vm.provision "shell", inline: $COMMANDS
end
  #-------------------------------------------------------------------------------------------------------------------
  config.vm.define "slve4" do |slave|
    slave.vm.box = "centos/7"
    slave.vm.hostname = "slave4"
    slave.vm.network :private_network, ip: "192.168.40.16"
    slave.vm.provider "virtualbox" do |v|
      v.memory = 2048
  end
  $COMMANDS = <<-"BLOCK"
  sudo sed -i "s/PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config;
  sudo systemctl restart sshd;
  BLOCK
  config.vm.provision "shell", inline: $COMMANDS
  end
  #-------------------------------------------------------------------------------------------------------------------
end