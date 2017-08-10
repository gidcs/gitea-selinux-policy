# gitea-selinux-policy
selinux policy for gitea


## install gitea selinux policy

```
curl -o gitea.te https://raw.githubusercontent.com/gidcs/gitea-selinux-policy/master/gitea.te
checkmodule -M -m -o gitea.mod gitea.te
sudo semodule_package -o gitea.pp -m gitea.mod
sudo semodule -i gitea.pp
rm gitea.*
```
