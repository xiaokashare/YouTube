
#  免费BT下载工具   TOP 4

#  1.Aria2

### Aria2 下载与安装

1. 进入 Aria2 官方下载页面：  https://aria2.github.io/   https://github.com/ziahamza/webui-aria2 
2. 下载最新版本的 Aria2 
3. 解压，我解压放在 D:\App\Aria2 下，然后该目录下新建四个文件：
   - Aria2.log （日志，空文件就行）
   - aria2.session （下载历史，空文件就行）
   - aria2.conf （配置文件）
   - HideRun.vbs （隐藏cmd窗口运行用到的）

### Aria2 的配置

**1**. 打开 aria2.conf ，复制以下内容到该文件：

```text
dir=D:\Download\

log=D:\App\Aria2\Aria2.log

input-file=D:\App\Aria2\aria2.session

save-session=D:\App\Aria2\aria2.session

save-session-interval=60

force-save=true

log-level=error

# see --split option

max-concurrent-downloads=5

continue=true

max-overall-download-limit=0

max-overall-upload-limit=50K

max-upload-limit=20

# Http/FTP options

connect-timeout=120

lowest-speed-limit=10K

max-connection-per-server=10

max-file-not-found=2

min-split-size=1M

split=5

check-certificate=false

http-no-cache=true

# FTP Specific Options

# BT/PT Setting

bt-enable-lpd=true

#bt-max-peers=55

follow-torrent=true

enable-dht6=false

bt-seed-unverified

rpc-save-upload-metadata=true

bt-hash-check-seed

bt-remove-unselected-file

bt-request-peer-speed-limit=100K

seed-ratio=0.0

# Metalink Specific Options

# RPC Options

enable-rpc=true

pause=false

rpc-allow-origin-all=true

rpc-listen-all=true

rpc-save-upload-metadata=true

rpc-secure=false

# Advanced Options

daemon=true

disable-ipv6=true

enable-mmap=true

file-allocation=falloc 

max-download-result=120

#no-file-allocation-limit=32M

force-sequential=true

parameterized-uri=true
```

**注意修改以下选项：**

dir=D:\Download\ （下载文件保存路径，改为你想要的）

log=D:\App\Aria2\Aria2.log （日志文件，路径D:\App\Aria2\改为你安装aria2的路径）

input-file=D:\App\Aria2\aria2.session

save-session=D:\App\Aria2\aria2.session

（这两个是记录和读取下载历史用的，断电和重启时保证下载任务不会丢失，如果有时aria2不能启动，清空这里面的内容就行了，路径D:\App\Aria2\改为你安装aria2的路径）

**2**. 编辑HideRun.vbs，并复制以下内容，注意修改D:\App\Aria2\为你的aria2安装路径：

```text
CreateObject("WScript.Shell").Run "D:\App\Aria2\aria2c.exe --conf-path=aria2.conf",0
```

要启动aria2，一定要点击这个文件，不要点击aria2c.exe。如果要开机启动，创建一个HideRun.vbs的快捷方式，放在”C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp“中即可。

**3**. 管理Aria 2 下载任务

- 首先我们要打开Aria2 的[WebUI] https://github.com/ziahamza/webui-aria2 
- 然后再页面的设置中将JSON-RPC Path设置为http://localhost:6800/jsonrpc
- 点保存，即可。

--------------------

# 2.Free download

**下载与安装**

源github地址： https://github.com/XIU2/TrackersListCollection 

 中文介绍地址：https://github.com/XIU2/TrackersListCollection/blob/master/README-ZH.md 

--------------------

# 3.比特彗星 (BitComet) 

**下载与安装** https://www.lanzoux.com/b073c7g4f 

便携版：不需要配置

官网版本配置教程：https://github.com/XIU2/TrackersListCollection/blob/master/README-ZH.md 



--------------------

# 4.uTorrent

下载地址（下载传统版，不要下载torrent web版）： https://www.utorrent.com/intl/zh/ 

#### Removing Ads.

 默认情况下，广告为“ True”，您只需将其值设置为“ False”即可将其禁用。例如，在过滤器上查找单词“ sponsored”。结果将显示一个名称为“ offers.sponsored_torrent_offer_enabled”的标志。通过将其值更改为“ False”将其关闭。 

对以下标志执行相同的操作：

- offer.sponsored_torrent_offer_enabled
- gui.show_plus_upsell
- offer.left_rail_offer_enabled
- offer.sponsored_torrent_offer_enabled
- gui.show_notorrents_node
- offer.content_offer_autoexec
- bt.enable_pulse

重新启动应用程序，以使更改生效。
