opencore-0.8.7，只测试了mac-12.6（Ventura），其它版本mac只能自己解决了



dell 3681 系统（只有cpu，内存，硬盘更换）

|          |                                                      |
| -------- | ---------------------------------------------------- 
| cpu      | intel 10700（8C/16T, 缓存16M，65瓦）                 |
| 主板     | 戴尔0MRC1X（LPC Controller B460芯片组）bios2020.5.14 |
| 内存     | 芝奇DDR4 2666， 单条32G，两条共64G                   |
|          |   |
| 主要硬盘 | 七彩虹CN700 1T（M.2 nvme pcie4）                     |
| 次要硬盘 | 三星SSD 870 QVO固态 2T（2.5寸sata）                  |
| 备用硬盘 | 希捷5T机械硬盘（2.5寸sata）                          |
|          |                                                      |
| 无线网卡 | 英特尔 Wireless-AC 3165 802.11ac 1x1 + 蓝牙 4.2      |
| 有线网卡 | Realtek RTL8111HS                                    |
| 集成显卡 | intel UHD Graphics 630                               |



dell 3681准系统（sff机箱），588元（闲鱼买的，机箱，电源，主板，散热器） ，

只有一个sata电源线，淘宝十块钱买个sata电源一分二， 无线网卡有线网卡和蓝牙都是主板自带的，

cpu：1190（淘宝，拿到是钎焊版，运气不错） ，

七彩虹1T：450元（天猫） ，

内存和其他硬盘是老机器拆的，整机差不多4500左右，



1.目前：有线，无线，声卡，显卡都正常

2.如果要更改启动等待时间，config.plist的TakeoffDelay字段，默认是3

3.bios关闭secure boot，以及SATA模式从默认的Raid on改为AHCI

4.问题比较大的是usb，启动可能报错：

AppleUSBHostPort::enumerateDeviceComplete_block_invoke: enumeration failed

https://apple.sqlsec.com/6-实用姿势/6-1.html

usb必须配置好（测试时：鼠标接2.0口，usb3的u盘接3.0口）

5.多系统：windows，macos共存：