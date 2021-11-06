---
# 标题
title: Linux服务器安装nodejs
# 置顶
top: false
# 打赏
reward: true
# 分类
categories:
- Linux
# 标签
tags:
- Linux
- node

---
Linux服务器安装nodejs

<!-- more -->
下载nodejs
=================

[nodejs官网](http://nodejs.cn/download/current/)，选择 `Linux 二进制文件 (x64)` 进行下载

![nodejs](/images/liunx-node.png)

上传包并解压
=================

我这里使用 `Xftp` 工具将包上传至服务器的/usr/local/src目录下

![nodejs](/images/liunx-node-upload.png)

登录 `Xshell`，访问/usr/local/src目录，执行解压命令

``` cmd
cd /usr/local/src
tar -xvf node-v14.18.1-linux-x64.tar.xz
```

解压完成
![nodejs](/images/node-jy.png)

检查解压后的文件夹资源是否完整，若不完整重新解压，如果还不行那就重新下载包重复以上操作
![nodejs](/images/node-sfwz.png)

全局引用
=================
创建软连接

``` cmd
ln -s /usr/local/src/node-v14.18.1-linux-x64/bin/npm /usr/local/bin
```

``` cmd
ln -s /usr/local/src/node-v14.18.1-linux-x64/bin/node /usr/local/bin
```

验证是否安装完成，依次执行以下命令，返回对应版本号表示安装完成
``` cmd
node -v
npm -v
```

![nodejs](/images/success-node.png)


