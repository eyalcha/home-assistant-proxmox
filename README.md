# Home Assistant Addons

- [Deepstack](https://github.com/johnolafenwa/DeepStack)
- [CompreFace](https://github.com/exadel-inc/CompreFace)
- [Frigate]()
- [Double-Take]()

## LXC

Install packages
```
apt update
apt install curl git zsh
```

Install docker 
```
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
```

Install docker compose
```
apt install docker-compose
```

Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## LXC NVR

Add to pve lxc conf (/etc/pve/lxc/xxx.conf)
```
lxc.mount.entry: /dev/bus/usb/002/ dev/bus/usb/002/ none bind,optional,create=dir 0,0
lxc.cgroup2.devices.allow: c 189:* rwm
lxc.apparmor.profile: unconfined
lxc.cgroup2.devices.allow: a
lxc.cap.drop: 
lxc.mount.auto: cgroup:rw
```




