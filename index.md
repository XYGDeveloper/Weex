## weex

Weex 致力于使开发者能基于通用跨平台的 Web 开发语言和开发经验，来构建 Android、iOS 和 Web 应用。简单来说，在集成了 WeexSDK 之后，你可以使用 JavaScript 语言和前端开发经验来开发移动应用。

Weex 渲染引擎与 DSL 语法层是分开的，Weex 并不强依赖任何特定的前端框架。目前 Vue.js 和 Rax 这两个前端框架被广泛应用于 Weex 页面开发，同时 Weex 也对这两个前端框架提供了最完善的支持。Weex 的另一个主要目标是跟进流行的 Web 开发技术并将其和原生开发的技术结合，实现开发效率和运行性能的高度统一。在开发阶段，一个 Weex 页面就像开发普通网页一样；在运行时，Weex 页面又充分利用了各种操作系统的原生组件和能力。

# 简介
TIP
Weex 是使用流行的 Web 开发体验来开发高性能原生应用的框架。

"Weex" 的发音是 /wiːks/, 和 "Weeks" 同音。

Weex 致力于使开发者能基于通用跨平台的 Web 开发语言和开发经验，来构建 Android、iOS 和 Web 应用。简单来说，在集成了 WeexSDK 之后，你可以使用 JavaScript 语言和前端开发经验来开发移动应用。

Weex 渲染引擎与 DSL 语法层是分开的，Weex 并不强依赖任何特定的前端框架。目前 Vue.js 和 Rax 这两个前端框架被广泛应用于 Weex 页面开发，同时 Weex 也对这两个前端框架提供了最完善的支持。Weex 的另一个主要目标是跟进流行的 Web 开发技术并将其和原生开发的技术结合，实现开发效率和运行性能的高度统一。在开发阶段，一个 Weex 页面就像开发普通网页一样；在运行时，Weex 页面又充分利用了各种操作系统的原生组件和能力。

# 概述
想初步了解 Weex 其实非常简单。

安装 Weex Playground. 在 Playground 里，你可以打开各种示例。
访问 Online Editor. 在这个网站上，你可以浏览、修改、新建各种基于 Vue.js 的单页面例子，并用 WeexPlayground 应用扫码查看实时效果。
TIP
尽管 Weex Playground 是 Apache Weex 的一部分，但 Online Editor 不是。

这里有一个使用 Weex 和 Vue.js 开发的最简单的例子。你可以大致了解 Weex 是如何工作的。

Weex Example

在 <template> 部分，包含了 <div> 元素，这个被广泛应用于 Web 页面中，在 Weex 里它也是一个通用的容器。<text> 元素就和普通的 HTML 不太一样了，它提供了显示文本的能力，在 Weex 上，所有文本必须放在 <text> 标签中。

在 <style> 部分，你可以定义各种 CSS 样式。需要注意的是，这些样式在 Weex 里只能作用于当前组件，scoped。

# 原生组件
在上面的例子中，<div> 和 <text> 在移动端上渲染出来的都是原生组件，充分利用了操作系统组件的能力与渲染速度。

Native Components

Weex 提供了一套基础的内置组件。你可以对这些基础组件进行封装、组合形成自己的组件；也可以创建自己的全新组件来包装操作系统提供的地图、视频等功能。可以访问 扩展 iOS 能力 和 扩展 Android 能力来了解如何去实现自定义组件。

在框架内部，Weex 使用原生组件来渲染，并尽可能保持多平台一致性。但在不同平台上，或多或少会有一些渲染、行为上的差异。比如对于 <switch> 组件，在不同平台上的视觉效果是不一致的。

Different switch

# 原生模块
对于那些不依赖于 UI 组件的功能，Weex 将它们包装成多个 模块，比如 动画模块。在前端代码中，使用 weex.requireModule('xxx') 引入一个模块，之后就可以调用它提供的各种方法。Weex 模块包装了网络、存储、剪切板、导航等各种功能供前端调用。比如你可以使用 stream 模块来获取 Vue.js 的 Star 数量。

Weex 已经提供了不少内置模块，同时也支持将 App 特有的功能包装成自定义模块提供给前端调用。如果想了解怎么做，可以浏览以下文档。

扩展 Web 组件
扩展 Android 能力
扩展 iOS 能力
# 一次编写，处处运行
Weex 的目标就是使用开发者基于一份代码，编写出可以运行在 iOS，Android 和 Web 上的应用，并最大化地提高开发效率和简化测试、构建、发布流程。

有一些场景，你可能仍然需要写一些平台相关的代码。Weex 提供 WXEnvironment 用来获取 Weex 运行的环境变量，浏览 Weex 环境变量，了解更多。

# 使用前端框架
Weex 应用需要依赖前端框架来编写，但 Weex 并没有绑定、限制在特定的框架上。目前 Vue.js 和 Rax 是最广泛应用于 Weex 开发的前端框架，也是目前功能最全、最稳定的方案。

Vue 和 Rax

Vue.js 是一个不断进化中的前端框架。
Rax 是提供类 React 语法和兼容性的前端框架。
Vue.js 和 Rax 都已经集成到 Weex 中，并默认提供。

将自己喜欢的前端框架和 Weex 进行结合是可以的，但并不是那么容易。我们也在不断开发和简化这种接入工作，如果想了解如何做，或有任何想法可以和我们联系。你也可以先阅读一下 使用前端框架 这篇文档了解它是做什么的。

# 下一步
当你看到这里的时候，我相信你已经了解了 Weex 的基本知识。下一步就是深入了解 Weex 的其他特性，并且动手试一试吧。

如果你想用 Weex 来开发自己的应用，请阅读

创建一个新的 App
集成到 iOS 应用
集成到 Android 应用
设置开发环境
如果你想为 Weex 贡献自己的力量，比如提交代码、修改文档或提交一些 Bug，可以阅读

How to Contribute
Bug Report Guidelines
# 开发
设置开发环境

使用 Online Editor 对 Weex 尝鲜是一个不错的选择，但如果你想更专业的开发 Weex，本节会教你如何搭建本地开发环境进行 Weex 开发。

# 安装依赖
Weex 官方提供了weex-cli 的脚手架工具来辅助开发和调试。

首先，你需要 Node.js 和 Weex CLI。

安装 Node.js 方式多种多样，最简单的方式是在 Node.js 官网 下载可执行程序直接安装即可。

更多安装方式可参考 Node.js 官方信息

TIP
通常，安装了 Node.js 环境，npm 包管理工具也随之安装了。因此，直接使用 npm 来安装 weex-toolkit, 你也可以通过 yarn 来进行安装。

国内的开发者推荐将npm镜像切换至 Taobao NPM 镜像 https://registry.npm.taobao.org。

运行下面的命令安装最新的beta版本工具：

# OSX环境
$ sudo chmod -R 777 /usr/local/lib/node_modules/
$ npm i -g weex-toolkit // 安装不要使用sudo执行
$ weex -v // 查看当前weex工具版本
# Windows环境
$ npm i -g weex-toolkit 
$ weex -v // 查看当前weex工具版本
安装结束后你可以直接使用 weex help 命令验证是否安装成功，它会显示 weex 支持的所有指令，同时，你也可以通过 weex doctor 命令检查你的本地开发环境。

# 初始化项目
然后初始化 Weex 项目：

$ weex create awesome-project
执行完命令后，在 awesome-project 目录中已经为我们生成了标准项目结构。

# 开发
进入项目所在路径，如果你在生成项目的时候选择了自动安装依赖，在进入项目后只需直接运行 npm start 就可以将项目完整跑起来，否则，你需要预先在项目中运行一下 npm install 安装项目所需依赖。

预览效果图

关于 Weex 语法部分，你可以直接参考 Vue Guide，这里不再重复介绍。如果您想了解有关技术详情的更多信息，请继续阅读下一节。


# 调试
概要

WARNING
Android Devtools for Apache Weex 是三方插件, 不由 Apache Weex 开发或维护。

Android Devtools for Apache Weex 能够方便调试 Weex 页面，但此功能离不开 Native端 的支持。本章将会详细说明 Android 端如何接入 Android Devtools for Apache Weex.

# 版本兼容
WeexSDK	Weex Inspector
0.16.0+	0.12.1
0.17.0+	0.13.2
0.18.0+	0.13.4-multicontext
0.19.0+	0.18.68
0.20.3.0-beta	0.20.3.0-beta
0.24.0+	0.24.2.4
0.26.0+	0.24.2.4
# Android接入指南
# 一、添加依赖
可以通过Gradle 或者 Maven添加对 Android Devtools for Apache Weex 的依赖, 也可以直接对源码依赖.

Gradle依赖.
dependencies {
   implementation 'com.taobao.android:weex_inspector:0.24.2.11'
}
或者

Maven依赖.
<dependency>
  <groupId>com.taobao.android</groupId>
  <artifactId>weex_inspector</artifactId>
  <version>0.24.2.11</version>
  <type>pom</type>
</dependency>
或者

源码依赖.
需要复制inspector目录到你的app的同级目录, 然后在工程的 settings.gradle 文件下添加 include ":inspector", 此过程可以参考playground源码的工程配置及其配置, 然后在app的build.gralde中添加依赖.

dependencies {
   compile project(':inspector')
}
需要引入okhttp
 dependencies {
    compile 'com.squareup.okhttp:okhttp:2.3.0'
    compile 'com.squareup.okhttp:okhttp-ws:2.3.0'
     ...
 }
# 二、调试开关（扫码开启调试/手动开启调试）
最简单方式就是复用Playground的相关代码,比如扫码和刷新等模块, 但是扫码不是必须的, 它只是与app通信的一种形式, 二维码里的包含DebugServer IP及bundle地址等信息,用于建立App和Debug Server之间的连接及动态加载bundle. 在Playground中给出了两种开启debug模式的范例.

范例1: 通过在XXXApplication中设置开关打开调试模式 
public class MyApplication extends Application {
  public void onCreate() {
  super.onCreate();
  initDebugEnvironment(true, "xxx.xxx.xxx.xxx"/*"DEBUG_SERVER_HOST"*/);
  //WXSDKEngine.reload();
  }
}

private void initDebugEnvironment(boolean enable, String host) {
  WXEnvironment.sRemoteDebugMode = enable;
  WXEnvironment.sRemoteDebugProxyUrl = "ws://" + host + ":8088/debugProxy/native";
}
这种方式最直接, 在代码中直接hardcode了开启调试模式, 如果在SDK初始化之前调用甚至连WXSDKEngine.reload()都不需要调用, 接入方如果需要更灵活的策略可以将initDebugEnvironment(boolean enable, String host)和WXSDKEngine.reload()组合在一起在合适的位置和时机调用即可.（如果不是初始化之前调用，n那么每次调用initDebugEnvironment后必须调用WXSDKEngine.reload()刷新Weex引擎）

范例2:通过扫码打开调试模式 
Playground中较多的使用扫描weex debugger生成的调试二维码的方式传递信息, 不仅用这种方式控制Debug模式的开关,而且还通过它来传入bundle的url直接调试. 应当说在开发中这种方式是比较高效的, 省去了修改sdk代码重复编译和安装App的麻烦.
拦截方式：

if (WXEnvironment.isApkDebugable()) {
  String devToolUrl = uri.getQueryParameter("_wx_devtool");
  if (!TextUtils.isEmpty(devToolUrl)) {
    WXEnvironment.sRemoteDebugProxyUrl = devToolUrl;
    WXEnvironment.sDebugServerConnectable = true;
    WXSDKEngine.reload(XXXXX.getApplication(), false);
  }
}
可选：调试刷新协议 
广播 ACTION_DEBUG_INSTANCE_REFRESH 在调试模式切换和 Chrome 调试页面刷新时发出，主要用来通知当前的 Weex容器以 Debug 模式重新加载当前页。在 playground 中的处理过程如下：
  public class RefreshBroadcastReceiver extends BroadcastReceiver {
    @Override
    public void onReceive(Context context, Intent intent) {
      if (IWXDebugProxy.ACTION_DEBUG_INSTANCE_REFRESH.equals(intent.getAction())) {
        //Do something
      }
    }
  }
# 科普
TIP
在以下的简介中，Android Devtools for Apache Weex 将简称为 Devtools

# Devtools组件介绍
Devtools扩展了Chrome Debugging Protocol, 在客户端和调试服务器之间的采用JSON-RPC作为通信机制, 本质上调试过程是两个进程间协同, 相互交换控制权及运行结果的过程. 更多细节还请阅读Weex Devtools Debugger的技术选型实录这篇文章.

客户端 Devtools 客户端作为aar被集成App中, 它通过webscoket连接到调试服务器,此处并未做安全检查. 出于安全机制及包大小考虑, 强烈建议接入方只在debug版本中打包此aar.

服务器 Devtools 服务器端是信息交换的中枢, 既连接客户端, 又连接Chrome, 大多数情况下扮演一个消息转发服务器和Runtime Manager的角色.

Web端 Chrome的V8引擎扮演着bundle javascript runtime的角色. 开启debug模式后, 所有的bundle js 代码都在该引擎上运行. 另一方面我们也复用了Chrome前端的调试界面, 例如设置断点, 查看调用栈等, 调试页关闭则runtime将会被清理.

调试的大致过程请参考如下时序图. debug sequence diagram
# 扩展

Weex 提供了扩展机制，可以根据自己的业务进行定制自己的功能。 主要分为两类扩展：

Module 扩展 非 UI 的特定功能。例如 sendHttp、openURL 等。
Component 扩展 实现特别功能的 Native 控件。例如：RichTextview，RefreshListview 等。
Adapter 扩展 Weex 对一些基础功能实现了统一的接口，可实现这些接口来定制自己的业务。例如：图片下载等。
JS全局变量自定义扩展
# JSEnv 扩展
# 接口

Map<String, Object> options = new HashMap();
options.set("testVlaue","hello");
//.... 
instance.render(pagename, template,options);

# 使用
var value = weex.config.testValue;

console.log(value);
# Module 扩展
Module 扩展必须继承 WXModule 类。
扩展方法必须加上@JSMethod (uiThread = false or true) 注解。Weex 会根据注解来判断当前方法是否要运行在 UI 线程，和当前方法是否是扩展方法。
Weex是根据反射来进行调用 Module 扩展方法，所以Module中的扩展方法必须是 public 类型。
同样因为是通过反射调用，Module 不能被混淆。请在混淆文件中添加代码：-keep public class * extends com.taobao.weex.common.WXModule{*;}
Module 扩展的方法可以使用 int, double, float, String, Map, List 类型的参数
完成 Module 后一定要在初始化时注册 WXSDKEngine.registerModule("myModule", MyModule.class); 否则会报类似错误：ReportException :undefined:9: TypeError: Object #<Object> has no method 'printLog'
示例如下：

public class MyModule extends WXModule {

  //run ui thread
  @JSMethod (uiThread = true)
  public void printLog(String msg) {
    Toast.makeText(mWXSDKInstance.getContext(),msg,Toast.LENGTH_SHORT).show();
  }

  //run JS thread
  @JSMethod (uiThread = false)
  public void fireEventSyncCall(){
   //implement your module logic here
  }
}
Register the module

WXSDKEngine.registerModule("MyModule", MyModule.class);
JS 调用如下：

<template>
  <div>
    <text onclick="click">testMyModule</text>
  </div>
</template>

<script>
  module.exports = {
    methods: {
      click: function() {
        weex.requireModule('MyModule').printLog("I am a weex Module");
      }
    }
  }
</script>
# Module 注册
registerModule(moduleName,moduleClass)

return(bool): 是否注册成功
moduleName(String): 模块名称
moduleClass(Class): 模块对应的class，创建module实例时使用
使用方式:

WXSDKEngine.registerModule("picker", WXPickersModule.class);
# Component 扩展
# wee x版本 >= 0.19.0
# 变更说明
WXDomObject 和 Layout 引擎被下沉到 WeexCore 中使用 C++ 实现，移除 Java 代码中的 WXDomObject。此次变更涉及 WXComponent 和 WXDomObject 的适配。

# 迁移指南
# setMeasureFunction 迁移
WXDomObject 中的 setMeasureFunction() 方法迁移至 WXComponent 中：

protected void setMeasureFunction(final ContentBoxMeasurement contentBoxMeasurement);
详见：com.taobao.weex.layout.ContentBoxMeasurement.java

ContentBoxMeasurement 示例请参考：WXText.java / setMeasureFunction() 注意：ContentBoxMeasurement 只支持叶子节点。

# WXComponent 接口变更
# getDomObject [移除]
由于 WXDomObject 下沉至 WeexCore 中，所以 getDomObject() 方法已被删除。

# 构造方法 [参数变更]
WXComponent 的构造方法删除了类型为 WXDomObject 的参数，新增了类型为 BasicComponentData 的参数，其余参数保持不变：

public WXComponent(WXSDKInstance instance, WXVContainer parent, int type, BasicComponentData basicComponentData);

public WXComponent(WXSDKInstance instance, WXVContainer parent, BasicComponentData basicComponentData);

# WXDomObject 接口变更
你无法在Java代码中访问和继承 WXDomObject，（ ImmutableDomObject 接口也已被删除）

WXDomObject 的部分方法被迁移至 WXComponent中，如需使用，如下：

# WXDomObject.getType() -> WXComponent.getComponentType() [迁移]
WXDomObject 中 的 getType() 方法用于获取组件类型（如：list、div、text、img...），迁移到 WXComponent 后，更名为：

public String getComponentType();
# 获取 Layout 结果的相关方法 [迁移]
获取 Layout 结果的6个方法从 WXDomObject 迁移至 WXComponent：

public float getCSSLayoutTop();
public float getCSSLayoutBottom();
public float getCSSLayoutLeft();
public float getCSSLayoutRight();
public float getLayoutWidth();
public float getLayoutHeight();
移除两个废弃接口：

public float getLayoutY();
public float getLayoutX();
# weex_sdk 版本 < 0.19.0
Component 扩展类必须继承 WXComponent.
Component 对应的设置属性的方法必须添加注解 @WXComponentProp(name=value(value is attr or style of dsl))
Weex sdk 通过反射调用对应的方法，所以 Component 对应的属性方法必须是 public，并且不能被混淆。请在混淆文件中添加代码 -keep public class * extends com.taobao.weex.ui.component.WXComponent{*;}
Component 扩展的方法可以使用 int, double, float, String, Map, List 类型的参数
完成 Component 后一定要在初始化时注册 WXSDKEngine.registerComponent("richText", RichText.class);
示例如下:

public class RichText extends WXComponent<TextView> {

    public RichText(WXSDKInstance instance, WXDomObject dom, WXVContainer parent) {
        super(instance, dom, parent);
    }

    @Override
    protected TextView initComponentHostView(@NonNull Context context) {
        TextView textView = new TextView(context);
        textView.setTextSize(20);
        textView.setTextColor(Color.BLACK);
        return textView;
    }

    @WXComponentProp(name = "tel")
    public void setTel(String telNumber) {
        getHostView().setText("tel: " + telNumber);
    }
}
注册你的组件：

WXSDKEngine.registerComponent("richText", RichText.class);
JS 调用如下：

<template>
  <div>
    <richText tel="12305" style="width:200;height:100">12305</richText>
  </div>
</template>
# 组件方法支持
从WeexSDK 0.9.5开始，你可以定义组件方法

在组件中如下声明一个组件方法
@JSMethod
public void focus(){
 //method implementation
}
注册组之后，你可以在weex 文件中调用

  <template>
  <mycomponent ref='mycomponent'></mycomponent>
  </template>
  <script>
  module.exports = {
    created: function() {
      this.$refs.mycomponent.focus();
    }
  }
  </script>
注:工程要添加依赖 compile 'com.squareup.picasso:picasso:2.5.2'

# Component 注册
#registerComponent(type,class,appendTree)
return(bool): 是否注册成功
type(String): 前端使用的对应标签
class(Class): 组件的class，在创建组件实例时调用
appendTree(bool): 渲染时判定逻辑，默认false
如果为true，则这个组件的子组件，整颗树建立、layout完后，整体一起刷新。
如果为false，则这个组件的子组件，每add一个，刷新一个。
使用方式:

WXSDKEngine.registerComponent("video", WXVideo.class, false);
#registerComponent(holder,appendTree，...names)
return(bool): 是否注册成功
holder(IFComponentHolder): 用于创建component的抽象工厂，默认使用__SimpleComponentHolder__。
appendTree: 同上
names(String ...): 前端使用的对应标签
使用方式:

WXSDKEngine.registerComponent(
              new SimpleComponentHolder(
                      WXText.class,
                      new WXText.Creator()
              ),
              false,
              "text"
      );
# Adapter 扩展
# 图片库Adapter
需要时集成接口 IWXImgLoaderAdapter，实现 setImage 方法。

示例如下：

public class ImageAdapter implements IWXImgLoaderAdapter {

  public ImageAdapter() {
  }

  @Override
  public void setImage(final String url, final ImageView view,
                       WXImageQuality quality, WXImageStrategy strategy) {

    WXSDKManager.getInstance().postOnUiThread(new Runnable() {

      @Override
      public void run() {
        if(view==null||view.getLayoutParams()==null){
          return;
        }
        if (TextUtils.isEmpty(url)) {
          view.setImageBitmap(null);
          return;
        }
        String temp = url;
        if (url.startsWith("//")) {
          temp = "http:" + url;
        }
        if (view.getLayoutParams().width <= 0 || view.getLayoutParams().height <= 0) {
          return;
        }
        Picasso.with(WXEnvironment.getApplication())
            .load(temp)
            .into(view);
      }
    },0);
  }
}
# Adapter 注册
# ImageAdapter
WEEX和图片库完全解耦，WEEX的图片加载，都是通过调用公共接口，由实现类决定调用哪个图片库

IWXImgLoaderAdapter: 根据url，load图片给某个view
IDrawableLoader(可选): 根据url，load图片给某个drawable.
# IWXImgLoaderAdapter
public interface IWXImgLoaderAdapter {
	void setImage(String url, ImageView view, WXImageQuality quality, WXImageStrategy strategy);   
}
WXImageQuality 图片质量的设置参数,有 LOW, NORMAL, HIGH, ORIGINAL 几种质量，默认为LOW.
WXImageStrategy 是一个扩展类参数，配置图像是否可以剪切isClipping、锐化isSharpen以及配置占位符placeHolder
# IDrawableLoader(可选)
  interface DrawableTarget {

  }

  interface StaticTarget extends DrawableTarget{
    void setDrawable(@Nullable Drawable drawable, boolean resetBounds);
  }

  interface AnimatedTarget extends DrawableTarget{
    void setAnimatedDrawable(@Nullable Drawable drawable);
  }

  void setDrawable(String url, DrawableTarget drawableTarget, DrawableStrategy drawableStrategy);
}
# IWXHttpAdapter
同ImageAdapter,WEEX和网络库也是解耦的，通过接口形式调用，由实现类决定调用哪个网络库。

public interface IWXHttpAdapter {
	void sendRequest(WXRequest request, OnHttpListener listener);
}
# WXRequest
paramMap(Map<String, String>): http自定义请求参数,比如(?a=1&b=2);
url(String): http请求的目标url
method(String): http请求方法 "post","get"
body(String): http请求body
timeoutMs(int): 请求超时时间，默认是3s
instanceId(String): （页面）id
# OnHttpListener
interface OnHttpListener {

	/**
	*  开始请求
	*/
	void onHttpStart();

	/**
	* 收到http header内容
	*/
	void onHeadersReceived(int statusCode,Map<String,List<String>> headers);

	/**
	*
	* @param 上传进度
	*/
	void onHttpUploadProgress(int uploadProgress);

	/**
	*
	* @param loadedLength 接收到的数据长度
	*/
	void onHttpResponseProgress(int loadedLength);

	/**
	* 请求结束
	* @param response 返回的response
	*/
	void onHttpFinish(WXResponse response);
}
# IWXUserTrackAdapter(可选)
打点相关，如果关注weex的打点，需要实现这个adapter

基础信息：sdk版本、jsbundle大小...
性能信息：sdk初始化时间、页面加载可交互时间、加载bundle时间...
public interface IWXUserTrackAdapter {
	void commit(Context context, String eventId, String type, WXPerformance perf, Map<String, Serializable> params);
}
# IActivityNavBarSetter
WXNavigatorModule的实现依赖这个接口，用来操作navigation.

使用方式:

WXSDKEngine.setActivityNavBarSetter(new IActivityNavBarSetter(){});   
# IWXStorageAdapter
WXStorageModule实现依赖这个接口，用来实现数据的存、取默认使用DefaultWXStorage实现

# IWXJSExceptionAdapter
WEEX的异常上报接口，包括

下载异常
白屏异常
js异常
降级异常
public interface IWXJSExceptionAdapter {
  void onJSException(WXJSExceptionInfo exception);
}
使用方式：

WXSDKEngine.setJSExcetptionAdapter(new TestExceptionAdapter());
# SDK混淆规则
若要在APP中使用混淆，请在相应的配置文件中添加如下规则：

-keep class com.taobao.weex.WXDebugTool{*;}
-keep class com.taobao.weex.devtools.common.LogUtil{*;}
-keepclassmembers class ** {
  @com.taobao.weex.ui.component.WXComponentProp public *;
}
-keep class com.taobao.weex.bridge.**{*;}
-keep class com.taobao.weex.dom.**{*;}
-keep class com.taobao.weex.adapter.**{*;}
-keep class com.taobao.weex.common.**{*;}
-keep class * implements com.taobao.weex.IWXObject{*;}
-keep class com.taobao.weex.ui.**{*;}
-keep class com.taobao.weex.ui.component.**{*;}
-keep class com.taobao.weex.utils.**{
    public <fields>;
    public <methods>;
    }
-keep class com.taobao.weex.view.**{*;}
-keep class com.taobao.weex.module.**{*;}
-keep public class * extends com.taobao.weex.common.WXModule{*;}
-keep public class * extends com.taobao.weex.ui.component.WXComponent{*;}
-keep class * implements com.taobao.weex.ui.IExternalComponentGetter{*;}
