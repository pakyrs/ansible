# A distro independent deployment Ansible playbook
#### based on ansible-pull

Works with Debian, RHEL and Arch based distributions. Debian / RHEL, takes advantage of debs, flatpaks and snaps to install certain apps that luckily on Arch are available via the AUR. Therfore the Arch deployment is much simpler but requires AUR module from Ansible Galaxy.

### If using Arch based distros:
The script leverages on the excellent `ansible-aur` module: https://github.com/kewlfft/ansible-aur
```
paru -S ansible-aur-git
OR
ansible-galaxy install kewlfft.aur
```

## Ansible-pull mode
Leverages the local.yml inventory file.
```
sudo apt install ansible -y
sudo ansible-pull -U https://github.com/pakyrs/ansible-pull.git
```
Use `--check` flag to have a "dry run" and verify if it will work for you.

## Ansible mode (using controlling device)

1) setup SSH and key exchange
2) run playbook from controlling machine to target

## Future plans
Integrating MacOS (brew) and Windows (chocolatey or winget), the latter for obvious reasons will have a different list of packages.

\\
