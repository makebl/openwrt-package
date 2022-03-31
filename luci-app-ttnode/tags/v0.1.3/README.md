# luci-app-ttnode

一个运行在openwrt下的甜糖星愿自动采集插件。

### Update Log 2020-12-10  

#### Updates

- NEW: 初始版本支持以下特性。
- NEW: 检测登录状态，可在本插件内登录。
- NEW: 获取用户信息。
- NEW: 定时自动采集。
- NEW: 定期自动提现。
- NEW: 运行结果推送到Server酱。


详情见[具体日志](./relnotes.txt)。 

### 介绍

脚本参考网友 Tom Dog 的 Python 版自动采集插件，使用LUA重写，基于LUCI的实现。 

### 如何使用

假设你的lean openwrt（最新版本19.07） 在 lede 目录下
```
cd lede/package/lean/  

git clone https://github.com/jerrykuku/luci-app-ttnode.git  

make menuconfig #Check LUCI->Applications->luci-app-ttnode

make package/lean/luci-app-ttnode/compile V=s  #单独编译luci-app-ttnode  

make -j1 V=s #编译固件
```

### 如何安装

🛑 [点击这里去下载最新的版本](https://github.com/jerrykuku/luci-app-ttnode/releases)  

1.先安装依赖  
```
opkg update
opkg install luasocket lua-md5 lua-cjson luasec
```
1.将luci-app-ttnode.ipk上传到路由器，并执行  opkg install /你上传的路径/luci-app-ttnode*.ipk

### 我的其它项目
Argon theme ：https://github.com/jerrykuku/luci-theme-argon  
Argon theme config  ：https://github.com/jerrykuku/luci-app-argon-config  
京东签到插件 ： https://github.com/jerrykuku/luci-app-jd-dailybonus  
Hello World ：https://github.com/jerrykuku/luci-app-vssr  
openwrt-nanopi-r1s-h5 ： https://github.com/jerrykuku/openwrt-nanopi-r1s-h5  
