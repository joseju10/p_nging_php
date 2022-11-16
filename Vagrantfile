Vagrant.configure("2") do |config|
    config.vm.define :servphp do |servphp|
      servphp.vm.box = "debian/bullseye64"
      servphp.vm.hostname = "servphp"
      servphp.vm.synced_folder ".", "/vagrant", disabled: true
      servphp.vm.network :private_network,
        :libvirt__network_name => "red1",
        :libvirt__dhcp_enabled => false,
        :ip => "10.0.0.1",
        :libvirt__forward_mode => "veryisolated"
    end
end
