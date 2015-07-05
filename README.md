Things that TOTALLY SUCKS. And how to disable them.

Pull requests are welcome.

---

## SELinux

```
> cat /etc/sysconfig/selinux
# This file controls the state of SELinux on the system.
# SELINUX= can take one of these three values:
#       enforcing - SELinux security policy is enforced.
#       permissive - SELinux prints warnings instead of enforcing.
#       disabled - SELinux is fully disabled.
SELINUX=permissive
# SELINUXTYPE= type of policy in use. Possible values are:
#       targeted - Only targeted network daemons are protected.
#       strict - Full SELinux protection.
SELINUXTYPE=targeted
```

## NetworkManager & systemd-networkd & systemd-resolved

```
systemctl stop NetworkManager
systemctl disable NetworkManager
systemctl stop systemd-networkd
systemctl disable systemd-networkd
systemctl stop systemd-resolved
systemctl disable systemd-resolved
```

Use [netctl](https://wiki.archlinux.org/index.php/Netctl)
