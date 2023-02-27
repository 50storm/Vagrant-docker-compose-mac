Vagrant.configure("2") do |config|
 # Centos7
 config.vm.box = "CentOS/7"

 config.vm.network :private_network, ip: "192.168.63.254"
 # dockerとdocker-composeを使える設定
 config.vm.provision "docker"
 config.vm.provision :docker_compose, compose_version: "1.29.2" #, yml: "docker-compose.yml"

 # macbook と centos7　とのシェアフォルダ
 SHARED_DIR = ENV['HOME'] + File::SEPARATOR +  "vmtest" + File::SEPARATOR + "shared"
 config.vm.synced_folder SHARED_DIR , "/mac_home", owner: "vagrant", group: "vagrant", create: "true"
end