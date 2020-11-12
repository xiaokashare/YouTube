### OpenWrt安装插件 这里以解锁网易云音乐插件为例

我使用的插件地址https://github.com/maxlicheng/luci-app-unblockmusic

1.打开插件地址，找到release，下载ipk文件，我这里下载的文件名是  luci-app-unblockneteasemusic_2.8-8_all.ipk

2.打开openwrt网页控制台，找到 系统》文件传输，把刚刚下载好的ipk文件上传到'/tmp/upload/'

3.打开远程控制台，找到   系统》TTYD终端，默认用户名root 默认密码 password


输入以下两行代码
```
cd /tmp/upload

opkg install luci-app-unblockneteasemusic_2.8-8_all.ipk
```

（输入opkg install l   然后按TAB键，自动补全）

这里就安装完成了，以下是使用方法，2步
```
- 点击“启用本插件”，打钩
- 下载CA根证书
```
安装结束


