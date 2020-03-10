# 配置Android Studio

## 修改生成文件的目录

### 修改.android目录

这个文件夹是由Android SDK配置模拟器生成的，也是最占空间的一个。

添加系统环境变量 `ANDROID_SDK_HOME` ，对应值为修改后 `.android` 的路径（如：`D:\SDKs\Android\.android`）。  
已创建的模拟器，它的默认位置还是在原位置，需要将其复制到目标目录，并修改模拟器的 `.ini` 配置文件。

### 修改.gradle目录

添加系统环境变量 `GRADLE_USER_HOME` ，对应值为修改后 `.gradle` 的路径（如：`D:\SDKs\Android\.gradle`）。  

### 修改.AndroidStudio目录

进入 `Android Studio` 安装目录下的 `bin` 目录，
取消 `idea.properties` 文件中 `idea.config.path` 和 `idea.system.path` 的注释，并修改其值