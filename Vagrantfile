hosts = {
  "host0" => "10.0.0.2",
}

Vagrant.configure("2") do |config|
  hosts.each do |name, ip|
    config.vm.define name do |machine|
      machine.vm.box = "trusty64"
      machine.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
      machine.vm.hostname = "%s.example.org" % name
      machine.vm.network :private_network, ip: ip
      machine.vm.provider "virtualbox" do |v|
          v.name = name
          v.customize ["modifyvm", :id, "--memory", 2048]
      end
    end
  end
end
