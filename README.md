
![](https://github.com/CarGuo/GSYVideoPlayer/blob/master/home_logo.png)

## 基于[IJKPlayer](https://github.com/Bilibili/ijkplayer)，实现了多功能的视频播放器。 (请仔细阅读下方各项说明，大多数问题可在下方找到解答)。

状态 | 功能
-------- | ---
**支持**|**边播边缓存，使用了[AndroidVideoCache](https://github.com/danikula/AndroidVideoCache)。**
**支持**|**列表播放；列表连续播放；重力旋转与手动旋转；视频本身rotation旋转属性。**
**支持**|**全屏切换动画效果；小窗口播放，可拖动。**
**支持**|**快播和慢播；网络视频加载速度。**
**支持**|**调整显示比例:默认、16:9、4:3、填充。**
**支持**|**播放时旋转画面角度（0,90,180,270）；镜像旋转。**
**支持**|**暂停前后台切换不黑屏；调整不同清晰度的支持。**
**支持**|**Https；IJKPlayer和EXOPlayer切换。**
**支持**|**锁定/解锁全屏点击功能；进度条小窗口预览（测试）。**
**支持**|**全屏与非全屏两套布局切换；弹幕功能。**
**支持**|**其他协议和编码concat、rtsp、crypto、mpeg等。**
**支持**|**没有任何操作控件的纯播放支持。**
**支持**|**DEMO演示获取视频第一帧等实现。**
待支持|**自带广告功能（目前需要自己实现）。**

[![](https://jitpack.io/v/CarGuo/GSYVideoPlayer.svg)](https://jitpack.io/#CarGuo/GSYVideoPlayer)
[ ![Download](https://api.bintray.com/packages/carguo/GSYVideoPlayer/gsyVideoPlayer/images/download.svg) ](https://bintray.com/carguo/GSYVideoPlayer/gsyVideoPlayer/_latestVersion)
[![Build Status](https://travis-ci.org/CarGuo/GSYVideoPlayer.svg?branch=master)](https://travis-ci.org/CarGuo/GSYVideoPlayer)

## 一、使用依赖

##### 新版本调整了代码结构，如更新后显示类路径错误，参考demo调整包路径即可。

### 1、JCenter 引入方法（推荐）

**你可以选择下面三种的其中一种，在module下的build.gradle添加。**

#### A、直接引入
```
//完整版引入
compile 'com.shuyu:GSYVideoPlayer:2.0.7'

```

#### B、添加java和你想要的so支持：

```
compile 'com.shuyu:gsyVideoPlayer-java:2.0.7'

//根据你的需求
compile 'com.shuyu:gsyVideoPlayer-armv5:2.0.7'
compile 'com.shuyu:gsyVideoPlayer-armv7a:2.0.7'
compile 'com.shuyu:gsyVideoPlayer-arm64:2.0.7'
compile 'com.shuyu:gsyVideoPlayer-x64:2.0.7'
compile 'com.shuyu:gsyVideoPlayer-x86:2.0.7'

```

#### C、支持其他格式协议的（mpeg，rtsp, concat、crypto协议）

A、B普通版本支持263/264/265等，对于mpeg编码会有声音无画面情况。
C 引入的so支持mpeg编码和其他补充协议，但是so包相对变大。
 
```
compile 'com.shuyu:gsyVideoPlayer-java:2.0.7' 

compile 'com.shuyu:gsyVideoPlayer-ex_so:2.0.7' 

```

### [--- 更多依赖方式请点击 - ](https://github.com/CarGuo/GSYVideoPlayer/blob/master/dependencies.md)

## 二、其他推荐

### * QQ群，有兴趣的可以进来（群里平时可能比较吵）：174815284 。
### * [RickText](https://github.com/CarGuo/RickText)
### * [LazyRecyclerAdapter](https://github.com/CarGuo/LazyRecyclerAdapter)

## 三、文档Wiki

### [--- 使用说明、接口文档 - 入口](https://github.com/CarGuo/GSYVideoPlayer/wiki)
### [--- 问题集锦 - 入口（大部分你遇到的问题都在这里解决） ](https://github.com/CarGuo/GSYVideoPlayer/blob/master/QUESTION.md)
### [--- 项目支持视频格式（如果遇上黑屏，没声音）](https://github.com/CarGuo/GSYVideoPlayer/blob/master/DECODERS.md)
### [--- IJKPlayer问题 - 入口](http://www.jianshu.com/p/220b00d00deb)　
### [--- IJKPlayer编译自定义SO - 入口](http://www.jianshu.com/p/bd289e25d272)　
### [--- 简书详解 （项目的基础）- 入口](http://www.jianshu.com/p/9fe377dd9750)
### [--- 版本更新说明 - 入口](https://github.com/CarGuo/GSYVideoPlayer/blob/master/UPDATE_VERSION.md)

## 四、运行效果

* ### 1、打开一个播放(旋转、镜像、填充)
<img src="https://github.com/CarGuo/GSYVideoPlayer/blob/master/11.gif" width="240px" height="426px"/>

* ### 2、列表/详情模式(动画、旋转、小窗体)

<div>
<img src="https://github.com/CarGuo/GSYVideoPlayer/blob/master/22.gif" width="240px" height="426px"/>
<img src="https://github.com/CarGuo/GSYVideoPlayer/blob/master/33.gif" width="240px" height="426px"/>
<img src="https://github.com/CarGuo/GSYVideoPlayer/blob/master/44.gif" width="240px" height="426px"/>
</div>

* ### 3、弹幕
<img src="https://github.com/CarGuo/GSYVideoPlayer/blob/master/55.gif" width="240px" height="426px"/>

* ### 4、进度条小窗口预览
<img src="https://github.com/CarGuo/GSYVideoPlayer/blob/master/07.gif" height="240px"/>

## 五、近期版本

### 2.0.7(2017-09-13）

* 优化增加了断网自动续连，需要为http前加上 "ijkhttphook:http://ssss"
* update ijk to 0.8.3
* 增加了demo中seekto精准定位，解决某些视频seek之后从头播放

### 2.0.6(2017-08-31)
* 调整了返回按键显示的问题。
* 修改了全屏可能出现缓冲不消失问题。
* 优化了双击问题。


### 更多版本请查阅：[版本更新说明](https://github.com/CarGuo/GSYVideoPlayer/blob/master/UPDATE_VERSION.md)

## 六、关于Issues

```
提问题前可先查阅上方文档和说明，请在Demo中复现问题。

问题说明：

1、说明那个Demo中哪个页面。
2、问题显现和重现步骤。
3、补充问题的视频流url，截图。
4、补充问题的机型，android版本。
```

## 七、混淆

```
-keep class tv.danmaku.ijk.** { *; }
-dontwarn tv.danmaku.ijk.**
-keep class com.shuyu.gsyvideoplayer.** { *; }
-dontwarn com.shuyu.gsyvideoplayer.**
```

## 依赖大小参考
建议使用ndk过滤，详细参考 [参考第四条 ： 4、NDK的so支持](http://www.jianshu.com/p/86e4b336c17d)
![](https://ooo.0o0.ooo/2017/06/15/5941f343a39f5.png)


## License

```
请参看IJKPlayer和AndroidVideoCache相关协议。
项目最开始是从jiecao过来的，只是后来方向不同，所以慢慢的也异化了。
```
