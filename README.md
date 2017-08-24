### 1.React Native是什么？

#####官方说法是这样的
React Native 是一个JavaScript 的框架，用来撰写实时的、可原生呈现iOS 和Android 的应用。 其是基于React的，而React 是Facebook 的用于构建用户界面的JavaScript 库

> ![](http://upload-images.jianshu.io/upload_images/2701853-d70d824c1ed125b6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

****
##### 我自己的看法是这样的
其实这东西从Native开发来说，相当于重新发明了一个浏览器渲染引擎并且套一个React的壳，从Web开发角度来说，就是把原来React的web组件成了原生组件来实现
***
### 2.哪些人在用

> ![](http://upload-images.jianshu.io/upload_images/2701853-b7c3b8fc886cd63e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

>![](http://upload-images.jianshu.io/upload_images/2701853-e58fdfcbb939f3c6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

上面是官方贴出的一些截图

目前我知道的一些项目:

1.[蚂蚁金服](https://mobile.ant.design/index-cn)
蚂蚁金服有一套开源的react组件,支持web还有rn端,这是一个可以参考的三端统一方案

2.[京东](http://www.infoq.com/cn/articles/jd-618-ReactNative-jingdong-practise)
京东JDReact,也实现了三端统一的方案,这篇文章,就京东现有架构做了一些解读

> ![](http://upload-images.jianshu.io/upload_images/2701853-dd48d93245ca6808.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


***

### 3.React Native的优势和劣势
#### 3.1React Native的优势：

(1)它最大的特点就是完全用JavaScript进行应用的开发，但是最终会渲染成原生的组件。对开发者来说，这意味着你拥有了Web开发的效率，同时兼顾了原生的性能

(2)相对Hybird app或者Webapp：

- 不用Webview，彻底摆脱了Webview让人不爽的交互和性能问题
- 有较强的扩展性，这是因为Native端提供的是基本控件，JS可以自由组合使用
- 本地直接加载,避免了网络请求造成的空白页
- 可以直接使用Native原生的「牛逼」动画。

(3)相对于Native app：

- 可以通过更新远端JS，直接更新app，不过这快成为各家大型Native app的标配了…
- 一套代码,ios android平台通用

(4)最后，社区活跃。除了Facebook之外，GitHub上有很多第三方的团队、个人、公司开发贡献了很多非常优秀的第三方组件，它的社区是非常健康、非常活跃的。

#### 3.2劣势：

- 扩展性仍然远远不如web，也远远不如直接写Native code（这个不用废话解释了吧）
- 从Native到Web，要做很多概念转换，势必造成双方都要妥协。最终web要用一套CSS的阉割版，Native要费劲地把这个阉割版转换成native原生的表达方式
- RN框架原生并不支持Web端。这意味着如果一个业务需要同时上Android、iOS和H5页面的话，那除了用RN之外，还需要用传统的H5或用ReactJS框架再做一次开发，这样效率是非常低的。
- Facebook给出的官方RN API不能完全满足业务快速的发展。它只给了一些很基础的API，但业务中经常会用到的一些多媒体，比如录音、录像、视频播放文件以及文件上传、压缩、加密等等，这些都没有提供。也就是说我们需要这些功能,还是需要原生的同学配合一起扩展的

***
#### 4 React native 常用组件和api

基础组件

> ![](http://upload-images.jianshu.io/upload_images/2701853-ce15ee092ac31337.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

用户交互组件

>![](http://upload-images.jianshu.io/upload_images/2701853-eac2c7cd1598ad42.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

列表组件

> ![](http://upload-images.jianshu.io/upload_images/2701853-951b963194163bd1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

ios特定组件和api

> ![](http://upload-images.jianshu.io/upload_images/2701853-cc04ae6f0c403906.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

android特定组件和api

> ![](http://upload-images.jianshu.io/upload_images/2701853-feda82d3cc165bc0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

其他功能组件和api

> ![](http://upload-images.jianshu.io/upload_images/2701853-19333380843f7cb4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](http://upload-images.jianshu.io/upload_images/2701853-1d91707c44449987.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

> 上面都是一些ReactNative官方提供的组件和API,
虽然官方有说一套代码代码实现andriod和ios平台的通用,
不过我们有时候还是需要在特定的场景做一些平台判断,
显示对应平台的代码,

如:

```
if(Platform.OS === 'android') {
   //安卓平台组件
}else if(Platform.OS === 'ios') {
  //ios平台组件
}
```

提供一些目前开源的扩展组件:

- **react-native 组件库** [https://js.coach/react-native/redux-saga-process](https://js.coach/react-native/redux-saga-process)

- **最佳轮播类组件** [https://github.com/leecade/react-native-swiper](https://github.com/leecade/react-native-swiper)

- A Native Picker with high performance. [https://github.com/beefe/react-native-picker](https://github.com/beefe/react-native-picker)


- 下拉刷新组件 [https://github.com/jsdf/react-native-refreshable-listview](https://github.com/jsdf/react-native-refreshable-listview)

- 模态框 [https://github.com/brentvatne/react-native-modal](https://github.com/brentvatne/react-native-modal)

- react-native-navbar [https://github.com/react-native-fellowship/react-native-navbar](https://github.com/react-native-fellowship/react-native-navbar)

- 滚动轮播组件 [https://github.com/appintheair/react-native-looped-carousel](https://github.com/appintheair/react-native-looped-carousel)

- HTML显示组件 [https://github.com/jsdf/react-native-htmlview](https://github.com/jsdf/react-native-htmlview)

- **Material React Native (MRN)** - Material Design组件库 [https://github.com/binggg/mrn](https://github.com/binggg/mrn)

- react-native-gitfeed - GitHub客户端(iOS/Android) [https://github.com/xiekw2010/react-native-gitfeed](https://github.com/xiekw2010/react-native-gitfeed)

- **React-Native-Elements** - React Native样式组件库 [https://github.com/react-native-community/React-Native-Elements](https://github.com/react-native-community/React-Native-Elements)

- **Shoutem UI** - React Native样式组件库 [https://github.com/shoutem/ui](https://github.com/shoutem/ui)

***

### 5.三端同一套代码实现的思考
**facebook官方的说法是react-native是为多平台提供共同的开发方式，而不是说一份代码，多处使用**

但是在正常的项目中,我们还是希望一套代码能够在ios,android,web端都可以通用的,这样可以保留我们h5的优势,大大提升开发效率

业界目前已经有一些比较成熟的案例的,
比如
1.[蚂蚁金服](https://mobile.ant.design/index-cn)
蚂蚁金服有一套开源的react组件,支持web还有rn端,这是一个可以参考的三端统一方案
2.[京东](http://www.infoq.com/cn/articles/jd-618-ReactNative-jingdong-practise)
京东这边也实现了一套三端统一的技术方案,不过目前没有可以参考的代码

> ![](http://upload-images.jianshu.io/upload_images/2701853-c8486084b37d8822.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

**这篇文章也提过
其实在业内三端融合也有广泛的研究，方案主要有三种。**

- 第一种方式，就是在RN跟ReactJS之上再封装一套轻量的跨平台的抽象层，像微软发布的ReactXP就类似于这样的架构。使用这种架构，意味着所有API、类、组件都不能用RN API，必须要用新的定义的接口，而且目前API支持也不是太多，还在完善中，所以没有采用这种方式。

- 第二种就是ReactJS做开发，之后通过工具转换成RN，这种方案适合于比较偏重H5业务的一些团队，因为他优先需要上的是H5页面，用户体验比较偏重H5。通过工具向RN转换其实是个有损转换，因为RN支持的样式实际比CSS样式少。从ReactJS向RN转换的话，可能会丢掉一些属性和布局。

- 第三种方案就是先用RN做开发，开发完之后再通过WebPack工具向ReactJS进行转换。这种方式的好处是可以优先保证RN中的体验，而且RN的样式支持是CSS的一个子集，这意味着从RN向ReactJS转换不会丢失功能和属性，所以业内更多的方案也是采用这种方式。GitHub上有一些类似的开源框架。但它们支持的组件并不是太全，不能完全覆盖我们的业务，所以我们自己实现了一套。包括之前说的所有的原生组件，它只有原生部分，我们也增加了JS部分的实现，使我们的框架可以完整、功能完全没有丢失地转化为Web页面。
***

目前我这边就第三种方案自己做了一个案例,中间运用到到淘宝团队做的一个开源库
[react-web](https://github.com/taobaofed/react-web)

实现效果如下:
- web端效果图

> ![](http://upload-images.jianshu.io/upload_images/2701853-4b6658668428ef83.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- android效果图

> ![](http://upload-images.jianshu.io/upload_images/2701853-cb8712665dc570cb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- ios效果图

> ![](http://upload-images.jianshu.io/upload_images/2701853-f6b4552d18b65550.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***
附上一些实现代码:


> ![](http://upload-images.jianshu.io/upload_images/2701853-67e8086b6c61a104.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

web文件夹里面就一个页面,还有webpack配置文件去打包

***

ios入口文件

```
/**
 * Sample React Native App
 * https://github.com/facebook/react-native
 * @flow
 */

import React, { Component } from 'react';
import {
  AppRegistry,
  StyleSheet,
  Text,
  View,
  Platform
} from 'react-native';

export default class reactnative extends Component {
  render() {
    return (
      <View style={styles.container}>
        <Text style={styles.welcome}>
          Welcome to React Native!
        </Text>
        <Text style={styles.instructions}>
          To get started, edit index.ios.js
        </Text>
        <Text style={styles.instructions}>
          Press Cmd+R to reload,{'\n'}
          Cmd+D or shake for dev menu
        </Text>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  welcome: {
    fontSize: 20,
    textAlign: 'center',
    margin: 10,
  },
  instructions: {
    textAlign: 'center',
    color: '#333333',
    marginBottom: 5,
  },
});

AppRegistry.registerComponent('reactnative', () => reactnative);
if(Platform.OS == 'web'){
  var app = document.createElement('div');
  document.body.appendChild(app);
  AppRegistry.runApplication('reactnative', {
    rootTag: app
  })
}
```
重点在这一段:
```
if(Platform.OS == 'web'){
  var app = document.createElement('div');
  document.body.appendChild(app);
  AppRegistry.runApplication('reactnative', {
    rootTag: app
  })
}
```
实现思路就是在平台为web的时候,如果引入Text组件,webpack将会
生成一个Text.web.js组件,web端的时候将会引用Text.web.js 去实现
Text组件的效果,同时会把css子集编译为web元素的行内样式.

###总结:当然这样的方案还是会有一定的局限性
- 首先就是目前我们依赖的react-web平台去做转换,
如果react-web不支持的组件,那么我们就无法实现转换
- 还有就是web端的事件处理机制跟移动端的不同点
- 移动端复杂的动画交互效果转换为web端还是有一定的局限性

案例源码我已经放到github上面
## [源码地址](https://github.com/ToNiQian/react-native-web)
上面的只是一个案例,如果后续想要真正的实现三端统一的功能,
还是需要自己去实现一套转换方案,这样组件就可以进行扩展.
实现思路可以借鉴淘宝的[react-web](https://github.com/taobaofed/react-web)

这边还有一个比较好的转换实现方案:
[react-native-web](https://github.com/necolas/react-native-web)
作者目前也在持续更新,目前关注已经有5000+
***

### 6.React Native的学习资源和开源app项目
#### 1.学习资源
- [reactnative官网](https://facebook.github.io/react-native/)
- [reactnative中文网站](http://reactnative.cn/docs/0.46/getting-started.html)
这2个网站可以用来学习reactnative环境的搭建,还有就是创建第一个reactnative项目
- [reactnative 最全案例汇总](https://github.com/jondot/awesome-react-native)

#### 2.开源app:
- 官方演示App [https://github.com/facebook/react-native/tree/master/Examples](https://github.com/facebook/react-native/tree/master/Examples)

- **Facebook F8 App** [https://github.com/fbsamples/f8app](https://github.com/fbsamples/f8app)

- **GitHub Popular(一个用来查看GitHub最受欢迎与最热项目的App)已上架**[https://github.com/crazycodeboy/GitHubPopular](https://github.com/crazycodeboy/GitHubPopular)

- 奇舞周刊 iOS 版（上架应用） [https://github.com/fakefish/Weekly75](https://github.com/fakefish/Weekly75)

- react-native-dribbble-app [https://github.com/catalinmiron/react-native-dribbble-app](https://github.com/catalinmiron/react-native-dribbble-app)

- **Gank.io客户端** [https://github.com/Bob1993/React-Native-Gank](https://github.com/Bob1993/React-Native-Gank)

- **Mdcc客户端(优质)** [https://github.com/Bob1993/mdcc-client](https://github.com/Bob1993/mdcc-client)

- **Leanote for iOS(云笔记)** [https://github.com/leanote/leanote-ios-rn](https://github.com/leanote/leanote-ios-rn)

-
 **ReactNativeRubyChina** [https://github.com/henter/ReactNativeRubyChina](https://github.com/henter/ReactNativeRubyChina)

- HackerNews-React-Native [https://github.com/iSimar/HackerNews-React-Native](https://github.com/iSimar/HackerNews-React-Native)

- React-Native新闻客户端 [https://github.com/tabalt/ReactNativeNews](https://github.com/tabalt/ReactNativeNews)

- **newswatch(新闻客户端)** [https://github.com/bradoyler/newswatch-react-native](https://github.com/bradoyler/newswatch-react-native)

- **buyscreen(购买页面)** [https://github.com/appintheair/react-native-buyscreen](https://github.com/appintheair/react-native-buyscreen)

- **V2EX客户端** [https://github.com/samuel1112/v2er](https://github.com/samuel1112/v2er)

- react-native-todo [https://github.com/joemaddalone/react-native-todo](https://github.com/joemaddalone/react-native-todo)

- react-native-beer [https://github.com/muratsu/react-native-beer](https://github.com/muratsu/react-native-beer)

- react-native-stars [https://github.com/86/react-native-stars](https://github.com/86/react-native-stars)

- **模仿天猫首页的app** [https://github.com/hugohua/react-native-demo](https://github.com/hugohua/react-native-demo)

- ReactNativeChess [https://github.com/csarsam/ReactNativeChess](https://github.com/csarsam/ReactNativeChess)

- react native 编写的音乐软件 [https://github.com/Johnqing/miumiu](https://github.com/Johnqing/miumiu)

- react-native-pokedex [https://github.com/ababol/react-native-pokedex](https://github.com/ababol/react-native-pokedex)

- CNode-React-Native [https://github.com/SFantasy/CNode-React-Native](https://github.com/SFantasy/CNode-React-Native)

- 8tracks电台客户端 [https://github.com/voronianski/EightTracksReactNative](https://github.com/voronianski/EightTracksReactNative)

- React-Native实现的计算器 [https://github.com/yoxisem544/Calculator-using-React-Native](https://github.com/yoxisem544/Calculator-using-React-Native)

- **房产搜索app** [https://github.com/jawee/react-native-PropertyFinder](https://github.com/jawee/react-native-PropertyFinder)

- **知乎专栏app** [https://github.com/LeezQ/react-native-zhihu-app](https://github.com/LeezQ/react-native-zhihu-app)


- Segmentfault 客户端 [https://github.com/fakefish/sf-react-native](https://github.com/fakefish/sf-react-native)

- 糗事百科app [https://github.com/stormhouse/QiuShiReactNative](https://github.com/stormhouse/QiuShiReactNative)

- 孢子社区app [https://github.com/Hi-Rube/baoz-ReactNative](https://github.com/Hi-Rube/baoz-ReactNative)

- **深JS app** [https://github.com/fraserxu/shenjs](https://github.com/fraserxu/shenjs)

- Den - 房屋销售app* [https://github.com/asamiller/den](https://github.com/asamiller/den)

- **Noder-cnodejs客户端** [https://github.com/soliury/noder-react-native](https://github.com/soliury/noder-react-native)

- 知乎日报Android版 [https://github.com/race604/ZhiHuDaily-React-Native](https://github.com/race604/ZhiHuDaily-React-Native)

- ziliun-react-native [https://github.com/sonnylazuardi/ziliun-react-native](https://github.com/sonnylazuardi/ziliun-react-native)

- react-native-weather-app [https://github.com/shevawen/react-native-weather-app](https://github.com/shevawen/react-native-weather-app)

- React Native Sample App(Navigation,Flux) [https://github.com/taskrabbit/ReactNativeSampleApp](https://github.com/taskrabbit/ReactNativeSampleApp)

- TesterHome社区app [https://github.com/qddegtya/A-ReactNative-TesterHome](https://github.com/qddegtya/A-ReactNative-TesterHome)

- Finance - 股票报价app [https://github.com/7kfpun/FinanceReactNative](https://github.com/7kfpun/FinanceReactNative)

- shopping - 购物app [https://github.com/bigsui/shopping-react-native](https://github.com/bigsui/shopping-react-native)

- zhuiyuan - 追源cms app [https://github.com/kazaff/ZhuiYuanDemo](https://github.com/kazaff/ZhuiYuanDemo)

- uestc-bbs-react-native - UESTC清水河畔RN客户端(with Redux) [https://github.com/just4fun/uestc-bbs-react-native](https://github.com/just4fun/uestc-bbs-react-native)

- **react-native-nw-react-calculator**(iOS/Android、Web、桌面多端) [https://github.com/benoitvallon/react-native-nw-react-calculator](https://github.com/benoitvallon/react-native-nw-react-calculator)

- react-native-nba-app [https://github.com/wwayne/react-native-nba-app](https://github.com/wwayne/react-native-nba-app)

- 开源中国的Git@OSC客户端 [http://git.oschina.net/rplees/react-native-gitosc](http://git.oschina.net/rplees/react-native-gitosc)

- rn_bycloud 帮瀛律师端app [https://github.com/liuchungui/rn_bycloud](https://github.com/liuchungui/rn_bycloud)

- **Reading App Write In React-Native（Studying and Programing** [https://github.com/attentiveness/reading](https://github.com/attentiveness/reading)

- 数独 - 重拾纯粹数独的乐趣 [https://github.com/nihgwu/react-native-sudoku](https://github.com/nihgwu/react-native-sudoku)

- Shop-React-Native [https://github.com/EleTeam/Shop-React-Native](https://github.com/EleTeam/Shop-React-Native)

- **掘金客户端** [https://github.com/wangdicoder/JueJinClient](https://github.com/wangdicoder/JueJinClient)

- cnblogs 客户端 [https://github.com/togayther/react-native-cnblogs](https://github.com/togayther/react-native-cnblogs)

注:加粗的项目,可以重点关注一下
***
### 总结:
**这些知识我自己的一些思考与理解,如果你有自己的想法还有理解,欢迎留言一起讨论**