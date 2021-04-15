# nas-packages

linkease & ddnsto for openwrt, arm and aarch64 and x86 supported

## 使用方法

把文件夹拷贝到Openwrt源代码的对应目录里面，拷贝之后为：

```
./package/feeds/luci/luci-app-ddnsto
./package/feeds/luci/luci-app-linkease

./package/network/services/linkease
./package/network/services/ddnsto

```

### make menuconfig 选择方法

```
make menuconfig

Network --->
Web Servers/Proxies --->
<*> ddnsto....................................... DDNS.to - the reverse proxy
<*> linkease....................................... LinkEase - the file cloud

LuCI --->
3. Applications --->
<*> luci-app-ddnsto.................................. LuCI support for ddnsto
<*> luci-app-linkease.................................. LuCI support for linkease
```

### 部分Openwrt老版本兼容性问题

ddnsto安装完成点击配置，需要手动运行命令：

```
/etc/init.d/ddnsto enable
```

