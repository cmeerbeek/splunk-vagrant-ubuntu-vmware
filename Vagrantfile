# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Use Ubuntu 18.04 VM box
  config.vm.box = "generic/ubuntu1804"

  # Configure hostname
  config.vm.hostname = "splunkans01"

  # Create private network with IP based on DHCP
  # Forward Splunk Web port
  # Forward Splunk MGMT port
  config.vm.network "private_network", type: "dhcp"
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.network "forwarded_port", guest: 8089, host: 8089

  # Sync data folder to /vagrant_data
  config.vm.synced_folder "data/", "/vagrant_data"

  # Set VM mem and num VCPU settings
  config.vm.provider "vmware_fusion" do |v|
    v.vmx["memsize"] = "2048"
    v.vmx["numvcpus"] = "2"
  end

  # Provision Splunk on running instance
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
  end

end