VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
#используем один ключ для всех машин
  config.ssh.insert_key = false

config.vm.define "vagrant1" do |vagrant1|
  vagrant1.vm.box = "generic/ubuntu1804"
  vagrant1.vm.network "forwarded_port", guest: 80, host: 8080
  vagrant1.vm.network "forwarded_port", guest: 443, host: 8443
end
config.vm.define "vagrant2" do |vagrant2|
  vagrant2.vm.box = "generic/ubuntu1804"
  vagrant2.vm.network "forwarded_port", guest: 80, host: 8081
  vagrant2.vm.network "forwarded_port", guest: 443, host: 8444
end
end
