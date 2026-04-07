Vagrant.configure("2") do |config|
    config.vm.box = "cdsn/debian13"

    config.ssh.insert_key = true

    config.vm.synced_folder ".", "/vagrant", disabled: true

    config.vm.provider :virtualbox do |v|
        v.memory = 256
        v.linked_clone = true

    end

# App Server 1
    config.vm.define "drup" do |app|
        app.vm.hostname = "drupal-vm.test"
        app.vm.network :private_network, ip: "192.168.56.4"
    end

end