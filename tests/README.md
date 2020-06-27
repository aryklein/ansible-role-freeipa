# Test IPA cluster on Vagrant (libvirt)

1. Set up Vagrant boxes:

```bash
$ vagrant-libvirt-plugin
$ vagrant up
```

2. Create an primary IPA node

```bash
$ ansible-playbook --limit primary ipa-primary.yml
```

4. Attach a replica IPA node

```bash
$ ansible-playbook --limit replica -e primary_ip=<x.x.x.x> ipa-replica.yml
```
