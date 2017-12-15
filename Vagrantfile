# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "macos_10.11"

  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"

  config.vm.synced_folder ".", "/vagrant", type: "rsync"  # the normal sharing uses guest extensions, which don't exist for macOS and virtualbox
#  config.vm.provision "shell", path: "update-os.sh"
#  config.vm.provision :reload
  config.vm.provision "shell", path: "bootstrap.sh", privileged: false
  config.vm.provision "shell", path: "build.sh"
end
