VAGRANTFILE_API_VERSION = "2"


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Use the same key for each machine
  config.ssh.insert_key = false
  config.vm.hostname = "mylocalhost"


  config.vm.define "vagrant1" do |vagrant1|
    vagrant1.vm.box = "cristiroma/centos-7-minimal"
    vagrant1.vm.network "private_network", ip: "192.168.10.1"
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "vvv"
      ansible.playbook = "provisioning/vagrant1/main.yml"
    end
  end
end

