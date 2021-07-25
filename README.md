# 1 
- ssh vào server
- tạo 1 file init: nhập `cat > init` sau đó dán nội dung lênh bên dưới:

```sh
sudo yum -y update
sudo yum install -y yum-utils
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

sudo yum install docker-ce docker-ce-cli containerd.io -y

sudo systemctl start docker

sudo curl -L "https://github.com/docker/compose/releases/download/1.28.6/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

sudo docker-compose --version

sudo systemctl enable /usr/lib/systemd/system/docker.service

sudo yum -y install git

```



# 2  Cấp quyền thực thi cho file:

```sh
 chmod 765 init 
```

[ với init là tên file vừa tạo]

# 3  run file

```sh
./init
```
