**2024年1月1日更新，解决图片显示问题。**

***

**一：使用SSR账号翻墙**

1、[Linux使用ss图形客户端Shadowosocks-QT5教程](https://shadowsockshelp.github.io/Shadowsocks/linux.html) (推荐)

2、[Linux客户端一键安装配置使用脚本(使用方法见注释)](https://github.com/the0demiurge/CharlesScripts/blob/master/charles/bin/ssr)

3、[Linux SSR 使用方法二](https://github.com/Turing2333/Detailed-tutorial-on-the-building-and-usage-of-SSR/blob/master/Instructions/Clients%20manual%20for%20each%20platform/Linux%20SSR%E7%9B%B8%E5%85%B3%E8%AF%B4%E6%98%8E.txt)

[全平台SS/SSR客户端下载汇总](http://www.mediafire.com/folder/sfqz8bmodqdx5/shadowsocks相关客户端)

[获取最新SS或SSR账号](https://github.com/Alvin9999/new-pac/wiki/ss%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7)
 
***

**二：使用v2ray账号**

**1、准备**

在[这里](https://github.com/v2ray/v2ray-core/releases/)下载适合系统的压缩包，并解压到 ~path/v2ray文件夹中。

编辑config.json配置文件，略。。。

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/1.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/2.png)

**2、配置**

将v2ray文件夹移动到 /usr/local/目录下，然后进入该目录

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/3.png)

  sudo mv /home/jacen/Downloads/v2ray /usr/local/v2ray

  cd /usr/local/v2ray/

创建配置文件目录 sudo mkdir /etc/v2ray

将配置文件复制到刚才创建的目录 sudo cp config.json /etc/v2ray/

运行v2ray

  cd /usr/local/v2ray/

  sudo ./v2ray --config=/etc/v2ray/config.json

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/4.png)

**3、设置开机启动**

执行以下命令，修改启动脚本

  cd /usr/local/v2ray/systemd/

  sudo vi v2ray.service

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/5.png)

将里面的ExecStart键值改为下面的 /usr/local/v2ray/v2ray -config /etc/v2ray/config.json

保存退出。

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2linux/a1.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/a2.png)

将文件复制到服务目录。 sudo cp v2ray.service /lib/systemd/system/

启动服务并开机自启

  sudo systemctl start v2ray.service

  sudo systemctl enable v2ray.service

停止服务 sudo systemctl stop v2ray.service

关闭开机自启

sudo systemctl disable v2ray.service

**注意事项**

关于配置文件，如果有win系统版的V2rayN软件，并成功配置了的，可以直接将其导出，替换压缩包里面的文件，不用修改即可直接使用。

代理设置应该和配置文件中保持一致

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/6.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/7.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/9.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/linux/10.png)

[点我获取最新v2ray账号](https://github.com/Alvin9999/new-pac/wiki/v2ray%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7)


***

**三：使用高速机场(付费)**

[w1.v2free.cyou](https://w1.v2free.cyou/auth/register?code=UsUP)是海外人士运营的高速翻墙服务，2020年开始已稳定运行3年。支持Windows/MAC/iOS/安卓/Linux/路由器等各平台高速翻墙：解锁大多数流媒体（Netflix、TVB、HKTV、ViuTV等），1080P高清视频、4K高清视频秒开，超低延迟。任意套餐的高速节点都支持访问openAI ChatGPT。

节点位置有台湾、香港、韩国、日本、美国、新加坡等，付费套餐节点包括v2ray节点和SS节点。截至2023年9月14日，节点共100个左右。

试用套餐5元（5天）、月付套餐A 20元、月付套餐B 39元、月付套餐C 58元、年付套餐A 168元、年付套餐A2 218元等，[套餐购买](https://w1.v2free.cyou/auth/register?code=UsUP)

详细介绍及购买方法：https://github.com/Alvin9999/new-pac/wiki/V2free%E6%9C%BA%E5%9C%BA

有问题也可以问在线客服。

***

**四：Linux使用Wine运行Windows软件**

图文教程可参考：

[Wine——在Linux上运行Windows软件](https://www.cnblogs.com/mo-wang/p/5183286.html)

[4种在Linux上运行Windows软件的方法]( https://jingyan.baidu.com/article/925f8cb8a1b813c0dde05698.html)

如果还有不清楚的地方，也可以自行搜素。当linux可以用windows软件的时候，这样可选择的空间就很大。

***

有问题或者有更好的Linux软件分享，都可以发邮件到海外邮箱进行反馈rebeccalane27@gmail.com