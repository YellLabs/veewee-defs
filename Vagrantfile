def create_vm(config, name, box)
    domain = "veewee"

    config.vm.define name do |c|
        c.vm.box            = box
        fqdn                = "#{name}.#{domain}"
        c.vm.host_name      = fqdn
        c.vm.customize      ["modifyvm", :id, "--name", fqdn]
    end
end

Vagrant::Config.run do |config|
    create_vm(config, :cent51p26, "centos51-puppet26")
    create_vm(config, :cent58p26, "centos58-puppet26")
    create_vm(config, :cent62p26, "centos62-puppet26")
    create_vm(config, :cent64p31, "centos64-puppet31")
end
