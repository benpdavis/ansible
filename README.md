# ansible
## debian
### debian - ansible setup
```
sudo apt update
sudo apt upgrade
sudo apt install ansible
sudo apt install sshpass
```

### debian - ansible push
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass`
### debian - ansible push with limit
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass --limit debian`
### debian - ansible push with limit and extra variables
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass --limit debian --extra-vars='upgrade_packages=true'`
### debian - ansible add ssh key to remote host
`ssh-copy-id HOSTNAME`
### debian - turn off ssh key checking
`export ANSIBLE_HOST_KEY_CHECKING=False`
### debian - turn on ssh key checking
`unset ANSIBLE_HOST_KEY_CHECKING`

## Windows
### windows - install wsl
`wsl --install`

### windows - reboot and run wsl
`wsl`

### wsl - ubuntu - ansible setup
```
sudo apt update
sudo apt upgrade
sudo apt install ansible
sudo apt install sshpass
```

### wsl - ubuntu - ansible push
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass`
### wsl - ubuntu - ansible push with limit
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass --limit debian`
### wsl - ubuntu - ansible push with limit and extra variables
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass --limit debian --extra-vars='upgrade_packages=true'`
### wsl - ubuntu - ansible add ssh key to remote host
`ssh-copy-id HOSTNAME`
### wsl - ubuntu - turn off ssh key checking
`export ANSIBLE_HOST_KEY_CHECKING=False`
### wsl - ubuntu - turn on ssh key checking
`unset ANSIBLE_HOST_KEY_CHECKING`