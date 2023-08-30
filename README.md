[![Docker Size](https://img.shields.io/docker/image-size/hanyaguang/baidunetdisk)](https://hub.docker.com/r/hanyaguang/baidunetdisk)
[![Docker Pulls](https://img.shields.io/docker/pulls/hanyaguang/baidunetdisk)](https://hub.docker.com/r/hanyaguang/baidunetdisk)

# 运行
```
docker run --name baidunetdisk \
  -v {配置文件夹}:/root/baidunetdisk \
  -v {下载文件夹}:/root/baidunetdiskdownload \
  -p {VNC端口}:5900 \
  -p {WEB端口}:6080 \
  -e VNC_SERVER_PASSWD='{VNC密码}' \
  hanyaguang/baidunetdisk:latest
```
样例:

   sudo docker run -d   --name=baidunetdiskv3.2    -p 6080:6080    -p 5900:5900    -v /srv/dev-disk-by-label-Exos1/appdata/baidunetdisk1:/config    -v /srv/dev-disk-by-label-Exos1/downloads/BaiduNetdisk1:/config/baidunetdiskdownload    --restart unless-stopped    hanyaguang/baidunetdisk:v3


## 通过VNC访问
默认端口为5900，使用任何VNC客户端连接，如[VNC® Viewer](https://www.realvnc.com/en/connect/download/viewer/)，[TightVNC](https://www.tightvnc.com/)。

## 通过浏览器访问
默认端口为6080。

http://IP:6080/vnc.html

添加firefox浏览器

添加 http://localhost:6080/baidunetdisk.html ，通过此网页可以复制黏贴百度共享链接地址.
