> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.bilibili.com](https://www.bilibili.com/read/cv5178548/)

废话不多说，直接开始，这里以 **GM220-S** 示范，步骤都差不多

1、打开浏览器，输入光猫的管理地址，一般是 **192.168.1.1**，具体的光猫背面有

![](http://i0.hdslb.com/bfs/article/8adbfd64bcadc060a80c0b6cacce92b67534cc36.png@1320w_770h.webp)光猫登录界面

2、输入**超级管理员**账号密码并登录，**不是**光猫背面的账号密码

账号：**CMCCAdmin**

密码：**aDm8H%MdA**

3、进入主界面，单击 “**网络**” 选项

![](http://i0.hdslb.com/bfs/article/f7ea11a60821e485c2bca61a5bf6e163c144eac8.png@1320w_1090h.webp)主界面

4、可以看到这样的界面，修改前记得**截图或拍照保存**，并**删除该配置**，

**前提是****要 知道 PPPoE 的用户名密码**，一般为用户名后六位，不确定的自己想办法

![](http://i0.hdslb.com/bfs/article/d599572cee0fc7f58de85afcb13c264800b8168e.png@1320w_1512h.webp)默认配置信息

5、选择 “**新建 WAN 连接**”

IP 协议版本选择 “**IPv4/v6**”

模式可选 “**PPPoE**” 或 “**桥模式**”

选择”PPPoE“是使用**光猫拨号上网**

选择 “桥模式” 则是使用**光猫 LAN 口 连接 路由器或电脑 拨号上网**

勾选 “**使能**” 复选框

根据需求绑定端口

勾选 “**DHCP 使能**” 复选框

去除 “**NAT**” 复选框

根据之前的截图填选 **业务模式**、**VLAN 模式**、**VLAN ID**、**MTU**、**用户名**、**密码**等信息

最后四项选则 **自适应**、**自适应**、**DHCPv6**、**DHCPv6** 即可

最后单击 “**创建**” 等待连接成功

![](http://i0.hdslb.com/bfs/article/bb7e3f9f669abe4295c3845747c89c7ce8ae50b1.png@1320w_1582h.webp)配置参数

6、回到 “**状态”** 主界面，单击 “**网络侧信息**”，选择”**IPv6 连接信息** “，即可看到 IPv6 连接情况

![](http://i0.hdslb.com/bfs/article/06893a41f94e4c147613bd69c696b4ad3315195b.png@1320w_1220h.webp)IPv6 连接信息

7、电脑上配置 IPv6 连接，选择 “**自动获取 IPv6 地址**”，DNS 填写光猫获取到的 DNS 即可

![](http://i0.hdslb.com/bfs/article/eee21048f96ca12c350223fe398b273987b878ab.png@1254w_1160h.webp)IPv6 配置网络连接

8、验证 IPv6 连接**是否有效**，并验证是否为**公网地址**

打开 “**IPv6 连接测试网站**”，再打开 **cmd** 输入 “**ipconfig/all**”

**临时 IPv6 地址**对的上**公网 IPv6 地址** 则为公网地址

关于打码，我觉得没必要，每次开机获取到的 IPv6 地址**都不一样**

![](http://i0.hdslb.com/bfs/article/ea14aada04bfe69ffc972f0414a44023af2c43a9.png@1320w_1234h.webp)验证公网 IPv6 地址

8、**网速测试**，我家办理的是 100M 移动宽带，150 块钱一年，测速结果如图所示

![](http://i0.hdslb.com/bfs/article/b8e80ba297532f2f9affa81ee2addc8f3fc28520.png@1320w_528h.webp)网速可超 100M

9、**网站测试**，因为运营商封了 80 端口，所以 80 端口用不了，这里用 7777 端口测试

![](http://i0.hdslb.com/bfs/article/ca95111eee7b9aaff21eb5b316f0553f03c2fe37.png@1320w_918h.webp)网站测试

在本机上使用 IPv6 地址打开是可以**正常访问**的

![](http://i0.hdslb.com/bfs/article/aedc56d0fb9af01042acd3916199ed78c11d2655.png@1320w_464h.webp)正常访问

手机用的是**联通 4G 网络**，可以获得 IPv6 地址

![](http://i0.hdslb.com/bfs/article/5cdb41300b23a9a0907e3fe870ad30e4b765f45c.png@1320w_2346h.webp)联通 4G 的 IPv6

在手机上可以**正常访问电脑建立的网站**

![](http://i0.hdslb.com/bfs/article/74d3179097c8bea7b93aaee9ac1c0099c51d12d8.png@1320w_2346h.webp)

10、**网站测速**，已知宽带上行速度 3.9MB/s，先来看看我这联通 4G 的网速

![](http://i0.hdslb.com/bfs/article/72f86cb8f47b238f83141c50eb8dfe67d8221ecb.png@1320w_2346h.webp)有点慢

随便放一个几百兆的文件测速

![](http://i0.hdslb.com/bfs/article/e40d200b6bf176bf63287aa400af2df510ba1141.png@1320w_460h.webp)340MB 的文件

手机打开网站进行下载，网速如图所示

![](http://i0.hdslb.com/bfs/article/2e830b3c301a23bbb767d0bf62810293b8ba9675.png@1320w_2346h.webp)速度还行，也就那样

**还有什么其他的玩法，你们自己去摸索吧**