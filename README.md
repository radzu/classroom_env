## About

rdacosta@redhat.com

This Ansible Playbook is suitable to be used in Red Hat Training classes and is tested on RHEL 8 and RHEL 9 environments. 

## Contributing

If you have ideas or requests - mail me at rdacosta@redhat.com

If you fancy contributing:

Create a branch -> Create a merge request -> Assign me as a reviewer.

## Getting started

Requires Ansible to be installed. 

```
git clone https://gitlab.com/rgdacosta/classroom_env.git

cd classroom_env

ansible-playbook playbook.yml
```

## Using

Check out these files for more information:

~/.bashrc

~/.vimrc

~/.tmux.conf

Resolution and gnome terminal profiles are set. 

For those who prefer a bigger font, set `biggerfont` as the default profile in the terminal preferences. `regularfont` is implemented as the default.

## OpenShift classes

The RHT_OCP4_ variables can be difficult to type at times, often resulting in typos and hindered success. 

Newer, simpler variables are available should `/usr/local/etc/ocp4.config` exist.

```
M=$RHT_OCP4_MASTER_API
WC=$RHT_OCP4_WILDCARD_DOMAIN
NS=$RHT_OCP4_NEXUS_SERVER
U=$RHT_OCP4_DEV_USER
P=$RHT_OCP4_DEV_PASSWORD
G=$RHT_OCP4_GITHUB_USER
Q=$RHT_OCP4_QUAY_USER
```

This means that you are able to use `$NS` when referring to the Nexus Server

If you forget what these variables are then use the function `my_ocp`

Logging into clusters:

```
lcl - local cluster login as admin (OpenShift courses <4.12)
mcl - managed cluster login as admin (DO480)
al - admin login (OpenShift courses >=4.12
dl - developer login
```

## Ansible classes

These aliases are there to simplify your training experience, they won't be available in certification exams. Of course you want to familiarize yourself with the actual commands before indulging in convenience :-)

# Ansible Core

```
ap - ansible-playbook
apsc - ansible-playbook --syntax-check
acd - ansible-config dump
av - ansible --version
aig - ansible-inventory --graph
```

# Ansible Navigator

```
anr - ansible-navigator run -m stdout
ansc - ansible-navigator run -m stdout --syntax-check
anch - ansible-navigator run -m stdout --check
ancd - ansible-navigator config dump -m stdout
anv - ansible-navigator --version
anig - ansible-navigator inventory --graph
```

## Productivity aliases

pastebin - Fancy taking a file from the training environment to the Internet? `cat $file | pastebin`. It will provide you with a short URL to grab your file from your local system.
decomment - Strips a file (typically a config file) of comments


