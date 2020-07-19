# 安装VPN

# v2ray+websocket(ws)+tls+nginx+cloudflare



### 1.准备域名（也可以不需要）为了把VPN流量伪装成正常网页

-  （免费域名教程）https://zhuanlan.zhihu.com/p/115535965 
- （付费域名教程） https://zhuanlan.zhihu.com/p/25627048 
- xx.daoyou321.xyz
- www.daoyou321.xyz

### 2. 购买VPS 推荐（系统推荐Debian，VPS推荐hostyun）

- 搬瓦工（ https://bandwagonhost.com/ ） 49.9刀/年   稳定+服务好，价格比较贵 50*7=350元 一个月30

- Hostyun 我目前在用的VPS  （个人推荐 https://my.hostyun.com/page.aspx?c=referral&u=17412  ）

   17元 *0.9 =15.3元  全场9折优惠码：hostyun 

- **PacificRack——pr**（ https://pacificrack.com/portal/aff.php?aff=2174 ） 6.25刀/年 我买的 500G   优惠码：[55OFF2020](https://pacificrack.com/portal/aff.php?aff=1) ，仅限年付，2年付，3年付    客服差，网速不稳定 

   


### 3.Clouldfare DNS解析设置

 https://www.imhunk.com/cloudflare-tutorials/ 

 https://zhuanlan.zhihu.com/p/56423186 

把DNS域名服务器地址，复制到购买域名的网站

这里以namesilo为例，登录namesilo，点开网页右上角 management my domain，对自己某个域名打钩，选择change namesevers（双向箭头图标），把clouldfare的两个DNS域名解析服务器地址，粘贴到这里。cmd ping 通就行了

### 4.一键安装  Debian系统

先升级

```
apt-get update -y && apt-get install curl -y
```

安装v2ray

BBR加速代码: BBR加速： 

```
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
```

 一键安装代码: 

```
 bash <(curl -L -s https://raw.githubusercontent.com/wulabing/V2Ray_ws-tls_bash_onekey/master/install.sh) | tee v2ray_ins.log 
```

 如果安装不了BBR请先运行以下代码： 

```
yum -y install wget
```



v2ray官方升级脚本：【 bash <(curl -L -s https://install.direct/go.sh) 】



### PC客户端下载

 https://github.com/2dust/v2rayN 

### 安卓客户端下载

 https://github.com/2dust/v2rayNG/releases 
 
### 客户端汇总

https://www.v2ray.com/awesome/tools.html
