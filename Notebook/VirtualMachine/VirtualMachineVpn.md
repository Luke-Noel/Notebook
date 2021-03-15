@[TOC](VMware上Ubuntu的网络配置)
# 问题描述
* 在Ubuntu浏览器Firefox中上网不成功
*  环境：VMware16pro，Ubuntu20.04.1 LST，Windows10家庭中文版，Clash for Windows V 0.9.6
# 网络代理的设置
## 必要信息的获取
1. 打开Windows的命令行，输入ipconfig，找到物理机的ip地址
	1） 使用win+R,打开运行界面 ，输入cmd，点击确定	
	![打开cmd界面](https://img-blog.csdnimg.cn/20210202200438367.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl81Mjc3ODkzNA==,size_16,color_FFFFFF,t_70)
	2） 输入ipconfig，找到IPV4地址（现在是2021年2月，不保证以后是 doge）![寻找IPV4地址](https://img-blog.csdnimg.cn/20210202203557193.png)
	3）找到并记录HTTP/HTTPS 代理端口
	4）找到并记录SOCKS代理端口
	5）打开局域网开关Allow LAN![在这里插入图片描述](https://img-blog.csdnimg.cn/20210202211116610.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl81Mjc3ODkzNA==,size_16,color_FFFFFF,t_70)

## 在Ubuntu进行设置
1. 找到虚拟机设置（settings）中找到网络设置（Network）![在这里插入图片描述](https://img-blog.csdnimg.cn/20210202210035549.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl81Mjc3ODkzNA==,size_16,color_FFFFFF,t_70)
2. 将Network Proxy中的设置从关闭（off）改为手动（Manual），并将信息填全，上数上述步骤没提到的以写入HTTP的内容（指HTTPS和FTP以及socks的ip和前两项的端口）
3. ![在这里插入图片描述](https://img-blog.csdnimg.cn/20210202211416320.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl81Mjc3ODkzNA==,size_16,color_FFFFFF,t_70)
4. 在VMware中进行设置
  在网络适配器中选择桥接模式
  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20210202212836356.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl81Mjc3ODkzNA==,size_16,color_FFFFFF,t_70)
  **——————————————————————————**
  至此，恭喜，你可以进行愉快的网络冲浪了
  Congratulation！