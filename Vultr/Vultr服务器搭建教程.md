## 购买
vultr注册地址：[vultr](https://www.vultr.com/)


## 一键部署
##### 登录后台
```bash
ssh root@ip
```
输入密码

##### CentOS6/Debian6/Ubuntu14 ShadowsocksR一键部署管理脚本
<code>1.可以设置部署管理不同端口的脚本</code>
在终端输入下面命令：
```bash
yum -y install wget

wget -N --no-check-certificate https://raw.githubusercontent.com/hombo125/doubi/master/ssrmu.sh && chmod +x ssrmu.sh && bash ssrmu.sh
```
备用脚本:
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssrmu.sh && chmod +x ssrmu.sh && bash ssrmu.sh 
```
安装后管理命令为：
```bash
bash ssrmu.sh
```

<code>2.部署管理脚本（没有限流功能）</code>
脚本一:
```bash
yum -y install wget
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh

```
备用脚本二:
```bash
yum -y install wget
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh
chmod +x shadowsocksR.sh
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log

```

## 一键加速 (centos6系统选择锐速加速，cenots7选择bbr加速)
##### centos6系统选择锐速加速
<code>1.先更换服务器内核</code>
```bash
yum -y install wget
wget --no-check-certificate https://blog.asuhu.com/sh/ruisu.sh && bash ruisu.sh

```
完成后会重启，2分钟后重新连接服务器，连上后开始第二步的操作。

<code>2.一键安装锐速</code>
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/91yun/serverspeeder/master/serverspeeder-all.sh && bash serverspeeder-all.sh

```

卸载的命令如下：
```bash
chattr -i /serverspeeder/etc/apx* && /serverspeeder/bin/serverSpeeder.sh uninstall -f
```

##### cenots7选择bbr加速
vultr服务器的centos6不支持bbr加速，但centos7系统支持bbr加速，所以如果你想用bbr加速教程，操作系统需要选择centos7
<code>谷歌BBR加速教程</code>
```bash
yum -y install wget
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh
chmod +x bbr.sh
./bbr.sh
```
最后输入y重启服务器，如果输入y提示command not found ，接着输入reboot来重启服务器，确保加速生效，bbr加速脚本是开机自动启动，装一次就可以了。

服务器重启成功并重新连接服务器后，输入命令
```bash
lsmod | grep bbr
```
 如果出现tcp_bbr字样表示bbr已安装并启动成功。

## 客户端下载
Windows SSR客户端:[4.7.0](https://github.com/shadowsocksr-backup/shadowsocksr-csharp/releases)

MAC SSR客户端:[Alpha test 3 for subscribe feature!](https://github.com/shadowsocksr-backup/ShadowsocksX-NG/releases)

安卓 SSR客户端:[update ssr-libev to latest version](https://github.com/shadowsocksr-backup/shadowsocksr-android/releases)

安卓 SS客户端:[v4.7.2](https://github.com/shadowsocks/shadowsocks-android/releases)

Windows SS客户端:[4.1.4](https://github.com/shadowsocks/shadowsocks-windows/releases)

MAC SS客户端:[Version 2.21](https://github.com/yangfeicheung/Shadowsocks-X/releases)

IOS SS客户端:[2.6.3](https://github.com/shadowsocks/shadowsocks-iOS/releases)


## 参考链接
1.[自建ss服务器教程](https://github.com/Alvin9999/new-pac/wiki/%E8%87%AA%E5%BB%BAss%E6%9C%8D%E5%8A%A1%E5%99%A8%E6%95%99%E7%A8%8B)

2.[用Vultr自己搭建ss/ssr服务器教程](https://www.vpscn.net/40.html)






