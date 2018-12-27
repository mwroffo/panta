Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |vb|
   vb.gui = false
  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get upgrade
    apt-get install -y wget curl build-essential emacs vim git libgtest-dev python zip gdb default-jdk
  SHELL
  config.vm.synced_folder "./", "/home/vagrant/shared"
end