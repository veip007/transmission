# transmission
```
docker run -d \
  --name=transmission \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Shanghai/China \
  -e TRANSMISSION_WEB_HOME=/transmission-web-control/ \
  -e USER=veip007 \
  -e PASS=github.com \
  -p 9091:9091 \
  -p 51413:51413 \
  -p 51413:51413/udp \
  -v /root/transmission/config:/config \
  -v /root/transmission/downloads:/downloads \
  -v /root/transmission/watch:/watch \
  --restart unless-stopped \
  veip007/transmission
  ```
  
  若架构为ARM则用下面的代码
  ```
  ```
docker run -d \
  --name=transmission \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Shanghai/China \
  -e TRANSMISSION_WEB_HOME=/transmission-web-control/ \
  -e USER=veip007 \
  -e PASS=github.com \
  -p 9091:9091 \
  -p 51413:51413 \
  -p 51413:51413/udp \
  -v /root/transmission/config:/config \
  -v /root/transmission/downloads:/downloads \
  -v /root/transmission/watch:/watch \
  --restart unless-stopped \
  veip007/transmission:arm64
  ```
  其中```  -e USER=veip007 \ ```
 ``` -e PASS=github.com \``` 为您的用户名和密码
 WEB访问地址为 IP:9091  防火墙记得端口放行9091和51413
