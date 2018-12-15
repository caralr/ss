一键脚本安装shadowsocks

支持系统

CentOS 6+

Debian 7+

Ubuntu 12+

一键搭建shadowsocks


1.git clone https://github.com/caralr/ss-wink

下载一键搭建ss脚本文件（直接在绿色光标处复制该行命令回车即可，只需要执行一次，卸载ss后也不需要重新下载）


如果提示bash: git: command not found，则先安装git：


Centos执行这个： yum -y install git

Ubuntu/Debian执行这个： apt-get update && apt-get -y install git


2.cd ss-wink


3.chmod +x ss-wink.sh


运行搭建ss脚本代码


4.ss-wink/ss-wink.sh -i caralr.club 2333


其中caralr.club换成你要设置的shadowsocks的密码即可 

这个caralr.club就是你ss的密码了，是需要填在客户端的密码那一栏的），密码随便设置，

最好只包含字母+数字，一些特殊字符可能会导致冲突。而第二个参数2333是端口号，也可以不加，不加默认是2333

相关操作ssr命令

启动：/etc/init.d/ss-wink start

停止：/etc/init.d/ss-wink stop

重启：/etc/init.d/ss-wink restart

状态：/etc/init.d/ss-wink status

查看ss链接：ss-wink/ss-wink.sh -sslink

修改配置文件：vim /etc/shadowsocks.json

配置文件路径：/etc/shadowsocks.json

日志文件路径：/var/log/shadowsocks.log

代码安装目录：/usr/local/shadowsocks

卸载ss服务

ss-wink/ss-wink.sh -uninstall
