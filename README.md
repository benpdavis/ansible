# ansible
## Windows
### windows - install wsl
`wsl --install`

### windows - reboot and run wsl
`wsl`

### wsl - ubuntu - ansible setup
`sudo apt update`

`sudo apt upgrade`

`sudo apt install ansible`

`sudo apt install sshpass`

### wsl - ubuntu - ansible push
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass`
### wsl - ubuntu - ansible push with limit
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass --limit debian`
### wsl - ubuntu - ansible push with limit and extra variables
`ansible-playbook site.yml -i hosts --ask-pass --ask-become-pass --limit debian --extra-vars='upgrade_packages=true'`
### wsl - ubuntu - turn off ssh key checking
`export ANSIBLE_HOST_KEY_CHECKING=False`
### wsl - ubuntu - turn on ssh key checking
`unset ANSIBLE_HOST_KEY_CHECKING`