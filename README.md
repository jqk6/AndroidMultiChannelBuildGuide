#一、修改APK META-INF打包（推荐）
原理：每次修改 APK META-INF

优点：速度快，不需要源代码和签名文件，使用简单

缺点：没有使用Android的productFlavors，无法利用flavors条件编译的功能

https://github.com/MasonLiuChn/BatchPackApk

https://github.com/GavinCT/AndroidMultiChannelBuildTool

#二、修改APK注释字段打包
原理：每次修改 APK注释字段

优点：速度快，不需要源代码和签名文件，使用简单

缺点：没有使用Android的productFlavors，无法利用flavors条件编译的功能

https://github.com/mcxiaoke/packer-ng-plugin

https://github.com/seven456/MultiChannelPackageTool

#三、gradle打包-manifestPlaceholders
描述：使用gradle 脚本打包

原理：批量build工程，处理 AndroidManifest.xml 文件时使用manifestPlaceholders

优点：稳定

缺点：耗时=一次build * 渠道数，需要提供源代码和签名文件

https://github.com/mcxiaoke/gradle-packer-plugin

#四、gradle打包-hook
描述：使用gradle 脚本打包

原理：批量build工程，处理 AndroidManifest.xml 文件时添加一个钩子(hook)替换渠道

优点：稳定

缺点：耗时=一次build * 渠道数，需要提供源代码和签名文件

https://github.com/umeng/umeng-muti-channel-build-tool/tree/master/Gradle

#五、友盟多渠道打包工具
描述：友盟提供的图形化打包工具

原理：方案一：每次反编译APK,修改 AndroidManifest.xml里的渠道号，重新打包签名；方案二：直接编辑二进制的AndroidManifest.xml文件，重新签名。

优点：图形化操作、不需要源代码、速度快

缺点：兼容性差、需要提供签名文件

https://github.com/umeng/umeng-muti-channel-build-tool

#六、Ant脚本打包
描述：这是一种比较陈旧的打包方式，记得我在2012年时是这样用的。

原理：批量build工程，build 前修改 AndroidManifest.xml里的渠道号。

优点：稳定

缺点：耗时=一次build * 渠道数，需要提供源代码和签名文件

https://github.com/MasonLiuChn/Android-Batch-Pack




