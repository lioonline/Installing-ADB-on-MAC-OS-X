#在 MAC OS X 安装 ADB (Android调试桥)
###什么是 ADB?
 Android调试桥（ adb ）是一个开发工具，帮助安卓设备和个人计算机之间的通信。 这种通信大多是在USB电缆下进行，但是也支持Wi-Fi连接。 adb 还可被用来与电脑上运行的安卓模拟器交流通信。 adb 对于安卓开发来说就像一把“瑞士军刀”。  

####通过 Homebrew 安装
```
brew install android-platform-tools
```
测试是否正常安装

```
adb devices
```

####手动安装
1、如果你以前安装过，请先删除老的文件


```
rm -rf ~/.android-sdk-macosx/
```

2、下载 android-sdk-macosx

下载地址：[developer.android.com](https://developer.android.com/sdk/index.html#Other)

3、将下载的文件解压并移动到 ~/.android-sdk-macosx

```
cd ~/Downloads(你的下载目录)/
unzip android-sdk*.zip
mv android-sdk-macosx/ ~/.android-sdk-macosx

```

4、运行 SDK Manager 

```
sh ~/.android-sdk-macosx/tools/android
```

5、根据你的需要选择，（我只需要Android SDK Platform-tools）［可选步骤］
6、选好后 Install 
7、环境变量设置

```
  echo 'export PATH=$PATH:~/.android-sdk-macosx/platform-tools/' >> ~/.bash_profile
```
8、更新配置文件

```
source ~/.bash_profile
```
9、测试是否正常安装
```
adb devices
```