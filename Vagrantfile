Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/trusty64"

  if defined?(VagrantVbguest::Middleware)
    config.vbguest.auto_update = true
  end

  config.vm.network "private_network", ip: "192.168.34.61"
  config.vm.synced_folder "./", "/vagrant", id: "vagrant-root",
  owner: "vagrant",
  group: "vagrant",
  mount_options: ["dmode=775,fmode=664"]

  config.vm.network :forwarded_port, guest: 5601, host: 5601
  config.vm.network :forwarded_port, guest: 9200, host: 9200
  config.vm.network :forwarded_port, guest: 9300, host: 9300

  config.vm.provision :shell, :path => "provision.sh"
end
