# Shadowsocks
copy from [shadowsocks/shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev)

# Downloads
- [shadowsocks](https://github.com/heal2017/shadowsocks/releases/download/latest/shadowsocks.zip)

# Install

install requirements
```shell
yum install gcc gettext autoconf libtool automake make pcre-devel asciidoc xmlto c-ares-devel libev-devel libsodium-devel mbedtls-devel -y
```

build and install shadowsocks
```shell
tar xvf shadowsocks-libev-3.3.5.tar.gz -C /opt
cd /opt/shadowsocks-libev-3.3.5
./configure
make && make install
```

# Startup ss-server

configure file [/etc/shadowsocks/server.json](https://github.com/heal2017/shadowsocks/config/server.json)

start ss-server
```shell
ss-server -c /etc/shadowsocks/server.json &
```

check listing port
```
ss -ano | grep '[port]'
```

