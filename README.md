# A distro independent deployment script
#### based on ansible-pull

Works with Debian, RHEL and Arch based distributions. Debian / RHEL, takes advantage of debs, flatpaks and snaps to install certain apps that luckily on Arch are available via the AUR. Therfore the Arch deployment is much simpler.

## PreRequisites
```
sudo apt install ansible -y
```

### If using Arch based distros:
The script leverages on the excellent `ansible-aur` module: https://github.com/kewlfft/ansible-aur
```
paru -S ansible-aur-git
OR
ansible-galaxy install kewlfft.aur
```

## Running
```
sudo apt install ansible -y
sudo ansible-pull -U https://github.com/pakyrs/ansible-pull.git
```
Use `--check` flag to have a "dry run" and verify if it will work for you.

## Future plans
Integrating MacOS (brew) and Windows (chocolatey or winget), the latter for obvious reasons will have a different list of packages.