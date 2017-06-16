## Welcome to ARES

Ares是一个基于JsBridge的混合移动开发框架，用于开发千米网的千米电商云APP等移动应用。Ares框架并不是一个单一的项目，是几种项目的结合体，这里有移动端底层的封装、增强的webview、jsbridge模块、应用模块管理系统等。

运用本框架开发APP以达到以下目的：

* 团队和业务之间解耦，独立开发，互不干扰，最后汇总成一个大型APP
* 业务模块开发者只需要很少，甚至不需要了解android／iOS底层特性，专注于业务即可
* 业务模块可以独立发布、升级、降级、维护
* 业务模块运行性能高于普通H5的性能
* 业务模块支持H5、ReactNative或者原生等开发方式
* 业务模块直接可以跳转和通信

### RN差分与热更新方案

现在每个业务模块（React Native实现）打出来的js bundle文件太大，同时通过React Container加载如此之大js bundle一瞬间会有短暂的白屏现象，急需优化

更多清[查看](blog/hotload.md)

### 业务模块按需与加载

为了让初次进入APP后初次加载某个业务模块能够不用等待下载时间，特此在APP刚进入时就开始下载所有的子模块js代码

更多清[查看](blog/preload.md)

## 业务模块间跳转和传参

这里讲述了业务模块之间是如果相互调用和传递数据的

更多清[查看](blog/moduleinteraction.md)

## APP管理系统解析

ARES配套了一个业务模块管理系统，只要提供每个业务模块的版本上传和状态管理，同时提供接口供前方APP查询所有的业务模块的汇总表

更多清[查看](blog/appmgr.md)
