# v2ray-heroku
> 部署
# 点击 [![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/xuiv/v2ray-heroku)，[一键部署到heroku](https://heroku.com/deploy?template=https://github.com/xuiv/v2ray-heroku)

客户端config.json设置如下：
```
{
  "log": {
    "loglevel": "warning"
  },
  "inbound": {
    "port": 1080,
    "listen": "127.0.0.1",
    "protocol": "socks",
    "domainOverride": ["tls","http"],
    "settings": {
      "auth": "noauth",
      "udp": true
    }
  },
  "outbound": {
    "protocol": "vmess",
    "settings": {
      "vnext": [{
        "address": "xxxx.herokuapp.com",
        "port": 443,
        "users": [{
          "id": "384caf82-f168-4f54-a91a-4e10795b6ded",
          "alterId": 64
        }]
      }]
    },
    "streamSettings": {
      "network": "ws",
      "security": "tls",
      "tlsSettings": {
        "allowInsecure": true,
        "serverName": null
      }
    },
    "mux": {
      "enabled": true,
      "concurrency": 8
    }
  }
}
```
