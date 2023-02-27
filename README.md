# Vagrantのプラグインが入ってなかったいれる
```
sudo vagrant plugin list
vagrant-docker-compose (1.5.1, global)
vagrant-hostsupdater (1.2.4, global)
vagrant-vbguest (0.31.0, global)
```
```
vagrant plugin install vagrant-docker-compose
vagrant plugin install vagrant-hostsupdater
vagrant plugin install vagrant-vbguest
```

# Vagrant + Centos7 + nginxで静的HTML環境(Mac)
```
sudo vagrant up
```

# umount /mntエラーが出たら
```
The following SSH command responded with a non-zero exit status.
Vagrant assumes that this means the command failed!

umount /mnt

Stdout from the command:



Stderr from the command:

umount: /mnt: not mounted
```

#　umount /mntエラー対応
 原因：kernelが古いらしい
```
 sudo vagrant ssh
 sudo yum -y update kernel
 exit
 sudo vagrant reload
```

# http接続確認 
ブラウザで以下のアドレスを入力
```
http://192.168.63.254:8080
```
