Vagrant.configure(2) do |config|
  config.vm.define "test" do |node|
        node.vm.box = "bento/centos-6.7"
        node.vm.hostname = "test"
        node.vm.network :private_network, ip: "192.168.1.100"
  end
  if Vagrant.has_plugin?("vagrant-proxyconf")
    config.proxy.http = "http://PROXY_HOST:PROXY_PORT/"
    config.proxy.https = "http://PROXY_HOST:PROXY_PORT/"
    config.proxy.no_proxy = "localhost,127.0.0.1,10.0.0."
  end
end
