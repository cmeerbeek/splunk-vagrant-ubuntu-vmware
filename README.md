# Vagrant setup for standalone Splunk instance
Vagrant setup for Splunk standalone machine using Ubuntu and VMWare provider.

## Getting Started

To get this VM up and running make sure you've installed [Vagrant](https://www.vagrantup.com/downloads.html) and the [VMWare provider](https://www.vagrantup.com/vmware/index.html).

This setup is based on the [generic Ubuntu 18.04 box](https://app.vagrantup.com/generic/boxes/ubuntu1804).

Make sure you put the correct Splunk deb-file in the **data** folder and change the provisioning/playbook.yml to reflect the correct file.

* Start the VM with: vagrant up --provider vmware_fusion.
* If you want to provision after setup run: vagrant reload --provision

## ChangeLog

See [CHANGELOG](CHANGELOG.md) for details.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Support

This app is developed in the open at [GitHub](https://github.com/cmeerbeek/splunk-vagrant-ubuntu-vmware). Use that repository-page to file issues if you have questions or need support.

## ToDo

Nothing for now.

## Copyright

 Copyright (c) 2020 Coen Meerbeek. See [LICENSE](LICENSE) for details.
