Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.synced_folder './project', '/var/www/html/project', owner: "www-data", group: "www-data"

  config.ssh.forward_agent = true

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provider/playbook.yml"
  end

end
