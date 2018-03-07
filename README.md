### 引言


----------
> 无线干扰器很简单也很廉价在某宝16-30元价格不等,没事的朋友可以买来玩玩,名字叫[ESP8266串口wifi模块 物联网 V3开发板]
> 这种WiFi deauth攻击由于WiFi自身协议漏洞导致无法预防，攻击只要是信号覆盖范围内的，几乎是100%有效的
> 本教程只用于测试,干扰他人网络是犯法行为,大家可不要尝试呀
## ESP8266串口wifi模块 物联网 V3开发板样图
![正面图](http://img.blog.csdn.net/20180307105131963?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
![背面图](http://img.blog.csdn.net/20180307105104810?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

## 制作教程开始

### 1.从我的github下载使用esp8266制作Deauth无线攻击的开源固件，是arduino开发的。
### *提示所需文件*
![这里写图片描述](http://img.blog.csdn.net/20180307114407107?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

 github里面包含了arduino IDE（1.arduino-1.8.2-windows.exe 开发工具）和固件源码（3.esp8266_deauther-master.rar）由于2.Arduino15-2开发包.rar体积较大我放在百度云上

 百度云下载地址:链接：https://pan.baidu.com/s/1T4zg0Oct1w0_2vd5k5UM0Q 密码：36io
###  2. 下载完毕后，解压。
###  3.双击1.arduino-1.8.2-windows.exe 安装arduino IDE。（如果你已经安装过arduino IDE，这步可以省略）

### 4、安装完毕后，打开arduino,菜单找到 文件—>首选项，点击红色区域进入SDK目录。我的路径是：C:\Users\Administrator\AppData\Local\Arduino15

![这里写图片描述](http://img.blog.csdn.net/20180307105945817?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
### 5.解压2.Arduino15-2开发包.rar ，把里面文件直接覆盖C:\Users\Administrator\AppData\Local\Arduino15下文件。

![这里写图片描述](http://img.blog.csdn.net/20180307110220614?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 6.找一根数据线把ESP8266开发板和电脑通过USB相连接,
![连接电脑](http://img.blog.csdn.net/20180307110736481?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
### 7.关闭Arduino重新启动

### 8.将ESP8266与电脑连接后，找到arduino IDE菜单里,工具—>开发板 在右侧出来的菜单中向下找，会找到一个 TPYBoard v202 点击选中。
![这里写图片描述](http://img.blog.csdn.net/20180307111049303?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
### 9. 解压3.esp8266_deauther-master.rar，

### 10.arduino IDE菜单栏 文件---->打开esp8266_deauther-master源码包esp8266_deauther\esp8266_deauther.ino

### 11.查看安装的usb转串的端口。打开电脑的设备管理器（这里是COM3）。
![这里写图片描述](http://img.blog.csdn.net/20180307112308508?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 12.   打开arduino IDE 工具--->端口，选择COM3（根据自己的实际端口号选择）
![这里写图片描述](http://img.blog.csdn.net/20180307112442515?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
### 13.  菜单栏下面的绿色图标菜单区，选择上传，开始编译，烧写固件
![这里写图片描述](http://img.blog.csdn.net/2018030711261422?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
#### 14.  查看最下方的日志区域
![这里写图片描述](http://img.blog.csdn.net/20180307112701542?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
![这里写图片描述](http://img.blog.csdn.net/20180307112726779?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 15.等待编译完成，出现上图信息（状态：变为“上传”）时，按住FLASH的同时，按一下RST按键松开，让ESP8266复位一下，继续按着FLASH,出现下面的信息时就可以松开FLASH按键了。

#### 提示::烧写固件时，板子上的蓝色小LED灯会一直快速闪烁。

#### 16.烧写完毕后，显示上传成功，板子上的蓝色小LED会停止闪烁。
![这里写图片描述](http://img.blog.csdn.net/20180307112935967?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 测试教程
#### 1. 成功烧写固件后，打开无线会搜索到名称为TPYBoard v202 的热点，密码默认tpyboard，进行连接。
#### 2. 连接成功后，打开浏览器输入192.168.4.1(电脑最好用谷歌浏览器夹加载快ps手机浏览器都无所谓) 。点击[我已阅读并理解上面的通知]（本次实验只用于测试实验，请谨慎使用）。
![这里写图片描述](http://img.blog.csdn.net/20180307113213126?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 3. 点击进来以后，首先扫描一下附近的wifi。点击[扫描]。
![这里写图片描述](http://img.blog.csdn.net/20180307113337418?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
#### 4.接下来我们选择一个wifi做一下攻击的测试
![这里写图片描述](http://img.blog.csdn.net/20180307113438112?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
#### 5.选择好后，点击最上方菜单栏[攻击]，进入攻击页面
![这里写图片描述](http://img.blog.csdn.net/20180307113514785?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
### 6.攻击方式有3种，Deauther、Beacon和Probe-Request。页面最下方有对这3种方式的介绍，Probe-Request实在不知道怎么翻译，大神们可以指点一下。
![这里写图片描述](http://img.blog.csdn.net/20180307113603121?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
#### 7.我们这次使用Deauther方式，阻止客户端连接，点击[START]开始攻击。
![这里写图片描述](http://img.blog.csdn.net/20180307113633464?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
#### 8.  找一个手机做一下实验，看是否还能连上boda。
![这里写图片描述](http://img.blog.csdn.net/20180307113721930?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjcxMTg4OTU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
#### 提示::  如果是第一次连接的话，会一直停在正在连接的界面上，无法连接成功。 如果原本连接着，会被强迫断线。
## 是不是很厉害,这样你就可以在不知道别人密码的情况下干掉对方网络,但是切记开玩笑可以但是不要用到非法用途上

## 作者
#### 作者: 孟庆岳
#### 官网: 百度搜索([shmily科技](http://weareshmily.top/ "shmily科技"))
#### CSDN博客:http://blog.csdn.net/qq_27118895
#### github:https://github.com/1294083463/