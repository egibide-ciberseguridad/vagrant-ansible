Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-20.04"

  config.vm.provider "vmware_desktop" do |v, override|
    override.vm.box = "bytesguy/ubuntu-server-20.04-arm64"
  end

  config.vm.define "server" do |server|
    server.vm.hostname = "server"
    server.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
end
