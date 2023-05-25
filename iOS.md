# iOS 常用开源项目学习

## NetworkExtension swift5 能用实例

https://github.com/vishal3kumar/SimpleTunnel

https://github.com/networkextension/SimpleTunnel

https://github.com/Lojii/Knot app抓包工具


https://github.com/cgcym1234/YYVPN  mac端抓包



[BearFree](https://github.com/zlyBear/BearFree) 
 
###  遇到 iOS 设置VPN页面显示”开发者必须更新“APP”才能链接“xx VPN”“

发现两种原因可能造成这种情况
1、appex因为某种原因没有打包安装在主应用上
2、info.plist文件中NSExtension的配置写错了
3、主应用和附加应用的identifier前缀不一致
总之，问题很可能出现在vpn相关配置文件上，仔细检查吧

finally, I fix it. Lower your Extension target "Build Settings" -> "iOS Deployment Target"->such as: iOS 9.0
可能是network extension的版本过高,你们把它调低一点...😄

### debug 调试
使用os_log import os.log
xcode > debug > attach to process by pid or name (display name)
控制台查看，选中进程显示即可。
