# SwiftUI-Guide
![image](https://github.com/fzhlee/SwiftUI-Guide/blob/master/images/swiftui-logo.png)<br/>
SwiftUI的80节教程及源码<br/>
所有课程基于Xcode 11 beta5，并在Xcode 11 beta5上编译通过。<br/>
当Xcode11正式版发布之后，会更新所有源码，以适配Xcode 11正式版。<br/>
<br/>
iOS开发相关互动课程列表，手把手学习iOS开发，App Store免费下载：<br/>
1、互动教程合集：https://apps.apple.com/cn/app/id1392811165<br/>
2、Xcode互动教程免费下载地址：https://itunes.apple.com/cn/app/id1063100471<br/>
3、Swift语言入门实例互动教程免费下载地址：https://itunes.apple.com/cn/app/id1320746678<br/>
4、app开发中的神兵利器免费下载地址：https://itunes.apple.com/cn/app/id1209739676<br/>
5、Objective-C语言应用开发互动教程免费下载地址：https://apps.apple.com/cn/app/id838877136<br/>
<br/>
![image](https://github.com/fzhlee/SwiftUI-Guide/blob/master/images/SwiftUI.png)
<br/>
# 第一章 常用控件<br/>
## 第一节：SwiftUI空白项目的创建步骤：<br/>
1、打开Xcode，然后使用菜单命令:File > New > Project命令，打开项目创建窗口。<br/>
2、在项目模板选择窗口中，选择Single View App模板，然后点击Next按钮，进入下一步设置窗口。<br/>
3、在项目配置窗口中，需要勾选Use SwiftUI复选框，然后填写其它的配置选项，点击Next按钮，完成项目的创建。<br/>
4、SwiftUI项目创建完成之后，其项目结构和代码功能如下图所示：<br/>
![image](https://github.com/fzhlee/SwiftUI-Guide/blob/master/images/SwiftUIXcode.png) 
<br/>
5、项目导航区：<br/>

<table>
	<thead>
		<tr>
			<th>文件名称</th>
			<th>说明</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>AppDelegate.swift</td>
			<td>提供didFinishLaunchingWithOptions等方法，用来处理程序启动之后的事件，或者响应来自外部的事件。</td>
		</tr>
		<tr>
			<td>SceneDelegate.swift</td>
			<td>设置应用程序窗口的rootViewController，并指定使用哪个ContentView作为rootViewController的rootView。</td>
		</tr>
		<tr>
			<td>ContentView.swift</td>
			<td>项目的初始界面，用户界面上的可视控件可以放置在此文件中。</td>
		</tr>
		<tr>
			<td>Assets.xcassets</td>
			<td>项目的资源文件，您可以在此处放置项目中所需的图片、颜色等资源。</td>
		</tr>
		<tr>
			<td>LaunchScreen.storyboard</td>
			<td>用来配置项目启动过程中所显示的内容。</td>
		</tr>
		<tr>
			<td>Info.plist</td>
			<td>项目的配置属性文件，配置产品名称、版本号、Build号、Bundle Identifier等项目。</td>
		</tr>
	</tbody>
</table>

6、代码编辑器：<br/>
	SwiftUI使用声明性语法，因此您可以简单地说明您的用户界面应该做什么。 <br/>例如，您可以编写需要包含文本字段的项目列表，然后描述每个字段的对齐方式，字体和颜色。 <br/>您的代码比以前更简单，更易于阅读，从而节省您的时间和维护。<br/>
```
import SwiftUI 		             //导入SwiftUI框架

struct ContentView: View {		 //定义一个名为ContentView的结构体，
    var body: some View {
        Text("Hello World")
    }
}

#if DEBUG
struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
#endif
```