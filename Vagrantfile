Vagrant.configure("2") do |config|
    config.vm.box = "hashicorp/precise32"
    config.vm.define :web do |web_config|
        web_config.vm.network "forwarded_port", guest: 8080, host: 8081
        #web_config.vm.network "private_network", ip: "192.168.50.10"
        web_config.vm.provision "shell", inline: "sudo apt-get update && sudo apt-get install -y puppet"
    end
end