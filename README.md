## Sliverlight 导航框架

### 特点

#### 按需加载 Silverlight 组件

与 SL 内置实现了真正意义的按需加载， 主程序可以非常小， 最小不超过 200 KB， 只有当点击链接之后， 才会去服务端下载
对应的组件， 每个组件文件只会下载一次。 如果要下载的组件引用了其它第三方的组件， 也会自动下载第三方组件， 下载第这些
时会自动过滤掉重复的组件。

### 几乎零配置

使用这个导航框架几乎不需要在客户端或服务端做任何配置， 整个加载过程是自动完成的， 你需要写的只是导航的菜单项。

## 使用方法

### 主程序

1. 添加对 AssemblyNavigation、 System.Windows.Controls.Navigation 的引用至项目；
2. 在主页面的 xaml 代码添加下面的 xmlns 引用：

    xmlns:sdk="http://schemas.microsoft.com/winfx/2006/xaml/presentation/sdk"
    xmlns:asmNav="clr-namespace:Beginor.AssemblyNavigation;assembly=Beginor.AssemblyNavigation"

3. 添加 Frame 控件并设置 ContentLoader， 代码如下：

    <sdk:Frame Name="MainFrame" Grid.Row="1" Source="MainApp.WelcomePage,MainApp">
       <sdk:Frame.ContentLoader>
          <asmNav:AssemblyNavigationContentLoader />
       </sdk:Frame.ContentLoader>
    </sdk:Frame>

### 模块

### 导航链接地址格式

## 注意问题

