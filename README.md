# nas-packages

linkease & ddnsto for openwrt, arm and aarch64 and x86 supported

## 使用方法

### 增加feed源

```shell
echo >> feeds.conf.default
echo 'src-git nas https://github.com/linkease/nas-packages.git;master' >> feeds.conf.default
./scripts/feeds update nas
./scripts/feeds install -a -p nas
```

### 集成软件包

```shell
make menuconfig
```

选择软件包
```plain
LuCI --->
3. Applications --->
<*> luci-app-ddnsto.................................. LuCI support for ddnsto
<*> luci-app-linkease.................................. LuCI support for linkease
```

### 构建固件
```shell
make
```
