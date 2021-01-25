# vulfocus-plus 
- forks from [vulfocus](https://github.com/fofapro/vulfocus)

## 全部使用docker安装
> 启动 `docker`
```bash
#!/bin/bash
rm -rf /var/run/docker*

# mount
mount -t nfs 10.27.106.174:/home/nfs /mnt/docker/ -o proto=tcp -o nolock

## docker
/usr/bin/dockerd --registry-mirror=https://hslzset5.mirror.aliyuncs.com -H unix:///var/run/docker.sock  -H tcp://0.0.0.0:2375 --data-root=/mnt/docker
```

## 安装
```bash
docker-compose up -d 

# 创建`mysql`数据库
docker exec -t mysql mysql -uroot -ptest@1q2w2e4R -e 'drop database vulcofus;'
docker exec -t mysql mysql -uroot -ptest@1q2w2e4R -e 'CREATE DATABASE `vulcofus` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;'

```

