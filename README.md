# HOME ASSISTANT on Raspberry 5

#### .vimrc

```
set nocompatible
set backspace=2
```

```
sudo cp .vimrc /root
```

####  /boot/firmware/cmdline.txt

```
... cgroup_memory=1 cgroup_enable=memory
```

### zsh



```bash
sudo apt install zsh

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"



```



#### K3S

```
curl -sfL https://get.k3s.io | sh -
sudo chown pi:pi /etc/rancher/k3s/k3s.yaml
```



#### k9s

```
wget https://github.com/derailed/k9s/releases/download/v0.32.5/k9s_linux_arm.deb
sudo dpkg -i k9s_linux_arm.deb
```

#### Helm

```
helm repo add duck-helm https://ducksify.github.io/duck-helm
kubectl create ns cloudflared
helm upgrade cloudflared duck-helm/cloudflared -n cloudflared --set auth.tunnelToken={ey...} --set replicaCount=1

helm repo add pajikos http://pajikos.github.io/home-assistant-helm-chart/

```

