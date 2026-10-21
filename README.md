# 快传 QuickDrop（Android 源码项目）

这是一个原生 Android Kotlin 项目原型：在同一 Wi‑Fi 局域网内通过 TCP 直接传输文件，不对图片或视频做压缩/转码；接收端写入 Android MediaStore 的 Pictures/QuickDrop 或 Movies/QuickDrop。

## 重要说明
- 当前交付的是**项目源码 ZIP，不是已编译 APK**。生成环境没有安装 Android SDK/Gradle，因此无法在这里真实编译、测试或签名 APK。
- 当前版本使用同一 Wi‑Fi 网络；尚未实现蓝牙/Wi‑Fi Direct 自动发现、断点续传、端到端加密或多设备配对。
- 仅建议在可信的私人 Wi‑Fi 网络使用。接收服务开放 TCP 8988 端口；此原型没有身份验证或加密。
- 这是可继续开发的 MVP 原型，正式使用前需在真机上测试不同 Android 版本、相册兼容性、超大文件、断线恢复及权限/后台行为。

## 编译
1. 在电脑安装 Android Studio（含 Android SDK 35）和 JDK 17。
2. 打开本项目目录，等待 Gradle Sync。
3. 选择 Build > Build APK(s)。
4. APK 通常输出在 `app/build/outputs/apk/debug/app-debug.apk`。

## 使用
1. 两台安卓手机连接同一 Wi‑Fi。
2. 接收手机打开应用，点“开启接收”，查看本机 IP。
3. 发送手机输入接收 IP，选择照片/视频，点“开始发送”。
