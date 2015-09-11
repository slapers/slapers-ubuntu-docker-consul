# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  
  config.ssh.forward_agent = true
  
  config.vm.define :docker1 do |box|
      box.vm.box = "ubuntu/trusty64"
      box.vm.provider "virtualbox" do |v|
        v.customize ["modifyvm", :id, "--memory", '1536']
      end
      box.vm.hostname = "docker1"
      box.vm.network :private_network, ip: "172.16.128.10"
      box.vm.network :forwarded_port, guest: 22, host: 22222
      box.vm.network :forwarded_port, guest: 80, host: 8080
      box.vm.network :forwarded_port, guest: 443, host: 8443
    
      box.vm.provision :shell, :inline => "sudo bash /vagrant/bootstrap/inject-ssh-keys.sh -k 'ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAvg0TbM+cz3wEf4hfNm+wMUuLe9X0Z21yG0/4Ha47kN7x7lDYfsnmSD2YdSruSdcZSSKRWDkX96bXPVVL//Awi/HzzVExucRej4HlETqvOGIMeaMZwQM/80+/vMGOphGehU1FMRdwuLVbvx/eajsaYRBwUrrt4ngsCH3Tfd6kbGu+cGYkfa8mJyxWXKfke1kcnYRa0LQSznym67l+6MHfyFDhsXhsoRq6GvF4sS4MocyeaSRidhStJMWmEhGgl52owvaQMRd1sBqXgiKkLyhvVPJqBypEfvXcLi9tScCPaxN0n0lqEQPbdz9xfz6qdTi2b4rvaogCOEvdxaDf7Ok3ow== stefan@rackboost.com'"      
      box.vm.provision :shell, :inline => "sudo service puppet stop && sudo rm -f /etc/rc2.d/S21puppet"
      box.vm.provision :shell, :inline => "sudo service chef-client stop && sudo rm -f /etc/rc2.d/S99chef-client"
    end
  
    
  config.vm.define :docker2 do |box|
      box.vm.box = "ubuntu/trusty64"
      box.vm.provider "virtualbox" do |v|
        v.customize ["modifyvm", :id, "--memory", '1536']
      end
      box.vm.hostname = "docker2"
      box.vm.network :private_network, ip: "172.16.128.11"
      box.vm.network :forwarded_port, guest: 22, host: 22223
      box.vm.network :forwarded_port, guest: 80, host: 8081
      box.vm.network :forwarded_port, guest: 443, host: 8444
  
      box.vm.provision :shell, :inline => "sudo bash /vagrant/bootstrap/inject-ssh-keys.sh -k 'ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAvg0TbM+cz3wEf4hfNm+wMUuLe9X0Z21yG0/4Ha47kN7x7lDYfsnmSD2YdSruSdcZSSKRWDkX96bXPVVL//Awi/HzzVExucRej4HlETqvOGIMeaMZwQM/80+/vMGOphGehU1FMRdwuLVbvx/eajsaYRBwUrrt4ngsCH3Tfd6kbGu+cGYkfa8mJyxWXKfke1kcnYRa0LQSznym67l+6MHfyFDhsXhsoRq6GvF4sS4MocyeaSRidhStJMWmEhGgl52owvaQMRd1sBqXgiKkLyhvVPJqBypEfvXcLi9tScCPaxN0n0lqEQPbdz9xfz6qdTi2b4rvaogCOEvdxaDf7Ok3ow== stefan@rackboost.com'"
      box.vm.provision :shell, :inline => "sudo service puppet stop && sudo rm -f /etc/rc2.d/S21puppet"
      box.vm.provision :shell, :inline => "sudo service chef-client stop && sudo rm -f /etc/rc2.d/S99chef-client"
  end
  
  
  config.vm.define :docker3 do |box|
      box.vm.box = "ubuntu/trusty64"
      box.vm.provider "virtualbox" do |v|
        v.customize ["modifyvm", :id, "--memory", '1536']
      end
      box.vm.hostname = "docker3"
      box.vm.network :private_network, ip: "172.16.128.12"
      box.vm.network :forwarded_port, guest: 22, host: 22224
      box.vm.network :forwarded_port, guest: 80, host: 8082
      box.vm.network :forwarded_port, guest: 443, host: 8445
  
      box.vm.provision :shell, :inline => "sudo bash /vagrant/bootstrap/inject-ssh-keys.sh -k 'ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAvg0TbM+cz3wEf4hfNm+wMUuLe9X0Z21yG0/4Ha47kN7x7lDYfsnmSD2YdSruSdcZSSKRWDkX96bXPVVL//Awi/HzzVExucRej4HlETqvOGIMeaMZwQM/80+/vMGOphGehU1FMRdwuLVbvx/eajsaYRBwUrrt4ngsCH3Tfd6kbGu+cGYkfa8mJyxWXKfke1kcnYRa0LQSznym67l+6MHfyFDhsXhsoRq6GvF4sS4MocyeaSRidhStJMWmEhGgl52owvaQMRd1sBqXgiKkLyhvVPJqBypEfvXcLi9tScCPaxN0n0lqEQPbdz9xfz6qdTi2b4rvaogCOEvdxaDf7Ok3ow== stefan@rackboost.com'"
      box.vm.provision :shell, :inline => "sudo service puppet stop && sudo rm -f /etc/rc2.d/S21puppet"
      box.vm.provision :shell, :inline => "sudo service chef-client stop && sudo rm -f /etc/rc2.d/S99chef-client"
  end
  
  
  config.vm.define :docker4 do |box|
      box.vm.box = "ubuntu/trusty64"
      box.vm.provider "virtualbox" do |v|
        v.customize ["modifyvm", :id, "--memory", '1536']
      end
      box.vm.hostname = "docker4"
      box.vm.network :private_network, ip: "172.16.128.13"
      box.vm.network :forwarded_port, guest: 22, host: 22225
      box.vm.network :forwarded_port, guest: 80, host: 8083
      box.vm.network :forwarded_port, guest: 443, host: 8446
  
      box.vm.provision :shell, :inline => "sudo bash /vagrant/bootstrap/inject-ssh-keys.sh -k 'ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAvg0TbM+cz3wEf4hfNm+wMUuLe9X0Z21yG0/4Ha47kN7x7lDYfsnmSD2YdSruSdcZSSKRWDkX96bXPVVL//Awi/HzzVExucRej4HlETqvOGIMeaMZwQM/80+/vMGOphGehU1FMRdwuLVbvx/eajsaYRBwUrrt4ngsCH3Tfd6kbGu+cGYkfa8mJyxWXKfke1kcnYRa0LQSznym67l+6MHfyFDhsXhsoRq6GvF4sS4MocyeaSRidhStJMWmEhGgl52owvaQMRd1sBqXgiKkLyhvVPJqBypEfvXcLi9tScCPaxN0n0lqEQPbdz9xfz6qdTi2b4rvaogCOEvdxaDf7Ok3ow== stefan@rackboost.com'"
      box.vm.provision :shell, :inline => "sudo service puppet stop && sudo rm -f /etc/rc2.d/S21puppet"
      box.vm.provision :shell, :inline => "sudo service chef-client stop && sudo rm -f /etc/rc2.d/S99chef-client"
  end
  
end
