Vagrant.configure("2") do |config|
  
  config.vm.define "sonar" do |sonar|
    sonar.vm.box = "sbeliakou/centos"
    sonar.vm.hostname = "sonar"
    sonar.vm.network "private_network", ip: "192.168.56.111"
    sonar.vm.provider "virtualbox" do |vb|
      vb.name = "sonar"
      vb.memory = "1024"
    end
    sonar.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end

end

