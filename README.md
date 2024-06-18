# Ansible Playbooks For Avant

`clone-playbook.yml` clones several relevant repositories to `~/work`

`ansible-playbook clone-playbook.yml` will run it

## Git

I'm trying to use ssh keys for everything so for my ssh config setup I need this block in `~/.ssh/config`

```bash
Host github-pypeaday
  Hostname github.com
  AddKeysToAgent yes
  IdentityFile ~/.ssh/pypeaday_github
  IdentitiesOnly yes
Host github.com-avant
  Hostname github.com
  AddKeysToAgent yes
  IdentityFile ~/.ssh/id_ed25519
  IdentitiesOnly yes

```

## Adding these just to get them over to my other machine

Host syncsort-prd
  #Hostname 10.92.2.179
  Hostname 10.92.5.181
  AddKeysToAgent yes
  User ec2-user
  # IdentityFile ~/.ssh/pci-prd-linux-kp.pub
  # IdentitiesOnly yes
  PasswordAuthentication no
Host syncsort-uat
  Hostname 10.92.11.113
  AddKeysToAgent yes
  User ec2-user
  IdentityFile ~/.ssh/pci-uat-linux-kp.pub
  IdentitiesOnly yes
  PasswordAuthentication no

