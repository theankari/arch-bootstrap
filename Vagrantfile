Vagrant.configure("2") do |config|
  config.vm.box = "archlinux/archlinux"
  config.vm.synced_folder ".", "/vagrant",
    type: "nfs",
    nfs_version: 4,
    nfs_udp: false,
    disabled: true

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = 4096
    vb.cpus = 4
    # vb.customize ["setextradata", :id, "GUI\/LastGuestSizeHint", "1920,1080"]
    vb.customize ["modifyvm", :id, "--vram", "256"]
  end
end
