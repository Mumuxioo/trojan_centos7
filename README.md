# trojan_centos7

一键脚本搭建科学上网Trojan梯子

下载sh脚本，执行
./trojan_centos7.sh

之后选1，回车，等待一下。过程中会提示需要输入域名，输入解析到本VPS的域名，然后回车。


第一次安装会失败，提示：
https证书没有申请成果，本次安装失败


这时候需要执行：
~/.acme.sh/acme.sh --register-account -m 你的邮箱@qq.com

在执行sh脚本
./trojan_centos7.sh

等待之后，会出现安装完成的信息，是一个指向你域名下的一个下载链接，右键选中复制下来，然后粘贴进浏览器下载，下载下来是一个trojan-cil压缩包，解压点开文件夹下usr->src->trojan-cil->config.json，记下remote_addr, remote_addr, password三项。

到这时候，用任意一个浏览器输入你刚才注册的域名，应该就可以看到一个网站（如果你到这看不到网页，就别往下做了，有两个原因，第一可能你买域名的时候解析地址填错了，第二，也是最大的可能性，这个ip的443端口已经被墙了，这时候就得去vultr重建一个vps了）。理解为它就是我们翻墙的掩护就好。

