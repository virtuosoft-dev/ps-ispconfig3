# ps-ispconfig3
A standard installation of [ISPConfig3](https://ispconfig.org) following the ["Perfect Server" HowtoForge guide](https://www.howtoforge.com/ispconfig-autoinstall-debian-ubuntu/). This project uses the trusted Ubuntu 20.04 Vagrant base box from [ubuntu/focal64](https://app.vagrantup.com/ubuntu/boxes/focal64).

This built box can be found on [Vagrant Cloud](https://app.vagrantup.com/Virtuosoft/boxes/ps-ispconfig3)

A repository regarding how this box was built, issue tracking, etc. [can be found on GitHub here](https://github.com/virtuosoft-dev/ps-ispconfig3).

## Credentials
The Ubuntu box root login can be performed via `sudo su` (as opposed to the ISPConfig directions in step "1. Log in to the server", stating `su -`); then we proceeded with the standard install. After the standard install of `wget -O - https://get.ispconfig.org | sh -s -- --use-ftp-ports=40110-40210 --unattended-upgrades` the following credentials were recorded:

```
[INFO] Your Mailman password is: rSTrGZarpFTW
[INFO] Your ISPConfig admin password is: A9Q3kAsjvP4XTuf
[INFO] Your MySQL root password is: BR4pjodRotfRoMUkjD6F
```

The firewall was then configured following step ["5. Setting up the firewall"](https://www.howtoforge.com/ispconfig-autoinstall-debian-ubuntu/). With this standard box configured, you can proceed to modify it to your needs. Be sure to set your external IP address in Vagrantfile (currently 10.0.1.3) *and* change your MySQL root password and ISPConfig admin password from the ones listed above!

Please support the ISPConfig3 project by purchasing a manual here:

[https://www.ispconfig.org/documentation/user-manual/](https://www.ispconfig.org/documentation/user-manual/)
