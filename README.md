# ubuntu-setup

Ansible scripts for setting up `ubuntu amd64/x86_64` machines with:

1. Apps/libs required for work
1. Apps/libs required for programming
1. General Stuff I like
1. ...

Mostly this can be done using `apt` but in certain cases these use `nix` to:

1. Avoid library incompatibilities (e.g. citrix vs Ubuntu 22.04)
1. Avoid snaps (where for some reason they have problems e.g. firefox snap does not work with keypassxc)

# Running

The scripts expect to run on the local machine; the default config has been setup to do this, 
see [ansible.cfg](ansible.cfg) and [hosts.yaml](hosts.yaml).

Some steps require elevation so become is required.

Run with:

```bash
ansible-playbook setup.xml
```
