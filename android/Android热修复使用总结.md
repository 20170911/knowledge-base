# 热修复框架使用对比总结

## 按照进化方式分类

native hook|java multidex|java hook|dex替换|混合/优化
-----------|-------------|---------|-------|-------
Dexposed|Qzone超级补丁|Robust|Amigo|Sophix
Andfix|QFix|Aceso|Tinker|-
Hotfix|Nuwa|-|-|-
-|RocooFix|-|-|-

其中 java multidex 中的方案原理均来自QZone, Nuwa参考QZone, RocooFix大部分代码来自于Nuwa，
随着Nuwa在三年前的停止更新，RocooFix也已停止更新，目前其他三个类别中以Andfix, Tinker, Robust可操作性更强
详细使用对比如下：

> 来自Tinker的对比的补充

方案对比 |Tinker|QZone|Andfix|Robust
--|--|--|--|--
类替换|yes|yes|no|no
SO替换|yes|no|no|no
资源替换|yes|yes|no|no
全平台支持|yes|yes|no|yes
即时生效|no|no|yes|yes
性能损耗|较小|较小|较小|较小
补丁包大小|较小|较大|一般|一般
开发透明|yes|yes|no|no
复杂度|较低|较低|复杂|复杂
Rom体积|Dalvik较大|较小|较小|较小
成功率|较高|较高|一般|最高
----|----|---|----|----
使用方式|命令行与gradle方式|--|命令行方式|gradle方式
社区活跃|很活跃|--|一般|活跃
受欢迎度（截至20200117）|14.7K|--|6.7K|3.5K
版本兼容|Android 2.x-8.x全平台，gradle3.2.x|--|Android2.3-7.0,gradle3.5.x|Android2.x-8.x,gradle3.5.x

- 热修复框架的选择可根据需求单独选用或结合使用
- 热修复技术只作为一种版本补救措施
- 由于Tinker框架的原理特性可作为小版本新需求发布，其他仅以修复BUG为主
