# Vagrant Configuration

Vagrant.configure(2) do |config|

    # Ubuntu 14.04 box
    config.vm.box = "ubuntu/trusty64"

    # Check for box updates ? default false
    config.vm.box_check_update = false

    # Set up private network
    config.vm.network "private_network", ip: "192.168.33.14"

    # Set up synced folders
    config.vm.synced_folder "html", "/var/www/html"

    # Provisioning
    config.vm.provision "shell", path: "./vagrant_conf/once.sh"
    config.vm.provision "shell", path: "./vagrant_conf/always.sh", run: "always"

end