# Android多渠道打包工具
## [VasDolly](https://github.com/Tencent/VasDolly)
VasDolly是一种快速多渠道打包工具，同时支持基于V1签名和V2签名进行多渠道打包。插件本身会自动检测Apk使用的签名类别，并选择合适的多渠道打包方式，对使用者来说完全透明。 V1.1.6版本已支持Android Gradle Plugin 3.0。
## [walle](https://github.com/Meituan-Dianping/walle)
瓦力通过在Apk中的APK Signature Block区块添加自定义的渠道信息来生成渠道包，从而提高了渠道包生成效率，可以作为单机工具来使用，也可以部署在HTTP服务器上来实时处理渠道包Apk的升级网络请求。
```
是专门针对增强版签名的一种多渠道打包方案 利用V2签名的校验方式不校验APK Signing Block并且忽略APK Signing Block中多余
的ID-VALUE这个特点，将渠道信息写到APK Signing Block中。

由于是直接对zip格式文件的操作，性能与添加zip注释方式相当

android 7.0 v2增强版签名
为了提高Android系统的安全性，Google从Android 7.0开始增加一种新的增强签名模式，从Android Gradle Plugin 2.2开始，
构建系统在打包应用后签名时默认使用APK signature scheme v2，该模式在原有的签名模式上，增加校验APK的SHA256哈希值，
如果签名后对APK作了任何修改，安装时会校验失败，提示没有签名无法安装
```
## [channelHelper](https://github.com/wswenyue/channelHelper)
基于walle工具的多渠道打包脚本
## [packer-ng-plugin](https://github.com/mcxiaoke/packer-ng-plugin)
packer-ng-plugin 是下一代Android渠道打包工具Gradle插件，支持极速打包，100个渠道包只需要10秒钟，速度是 gradle-packer-plugin 的300倍以上，可方便的用于CI系统集成，同时提供命令行打包脚本，渠道读取提供Python和C语言的实现。
```
添加zip注释方式

利用android签名不校验zip文件注释信息的漏洞，apk本质是一个zip包，将渠道信息写入zip文件注释内将不受签名限制 
打包签名一个无渠道信息的apk完成后，复制此apk并将不同渠道信息字符串分别写入新生成的apk文件 
100个渠道包只需10秒
```
## [这个一个关于怎样在Android Stuido里使用productFlavors的示例](https://github.com/lendylongli/ProductFlavorsAdDemo)
