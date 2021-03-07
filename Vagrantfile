# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "scptcgjpjwiki/stjj-aic-vm"

  config.vm.network "forwarded_port", guest: 443, host: 443, host_ip: "127.0.0.1"

  # 共有フォルダ設定。ここでコケる場合はvagrant plugin install vagrant-vbguestを叩く（多分）
  # サーバーサイドのローカルリポジトリと共有
  config.vm.synced_folder "../stjj-aic-server", "/home/vagrant/repo/stjj-aic-server"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 1
    vb.memory = "600"
  end

end
