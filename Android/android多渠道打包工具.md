# Android多渠道打包工具
## [VasDolly](https://github.com/Tencent/VasDolly)
VasDolly是一种快速多渠道打包工具，同时支持基于V1签名和V2签名进行多渠道打包。插件本身会自动检测Apk使用的签名类别，并选择合适的多渠道打包方式，对使用者来说完全透明。 V1.1.6版本已支持Android Gradle Plugin 3.0。
## [walle](https://github.com/Meituan-Dianping/walle)
瓦力通过在Apk中的APK Signature Block区块添加自定义的渠道信息来生成渠道包，从而提高了渠道包生成效率，可以作为单机工具来使用，也可以部署在HTTP服务器上来实时处理渠道包Apk的升级网络请求。
## [packer-ng-plugin](https://github.com/mcxiaoke/packer-ng-plugin)
packer-ng-plugin 是下一代Android渠道打包工具Gradle插件，支持极速打包，100个渠道包只需要10秒钟，速度是 gradle-packer-plugin 的300倍以上，可方便的用于CI系统集成，同时提供命令行打包脚本，渠道读取提供Python和C语言的实现。
