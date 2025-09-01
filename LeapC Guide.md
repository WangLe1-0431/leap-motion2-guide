# LeapC & Python Guide By WangLe1_

LeapC是用于驱动LeapMotion的官方C API。
可通过LeapC在C程序中直接运行，对于Python的支持需要通过`leapc-python-binding-main`来进行，前往该项目请点击[此处](https://github.com/ultraleap/leapc-python-bindings)。

注意：**仅支持Python3.8**

## 概述

LeapC 库充当您的应用程序和手势追踪服务之间的中介。LeapC 实现了一个消息队列，用于向该服务发送追踪、图像和状态消息。

一旦与服务建立连接，您的应用程序就会使用该`LeapPollConnection()`函数来驱动应用程序定义的消息泵。每次调用都会`LeapPollConnection()`返回下一条消息，或者阻塞指定的超时时间。

您的泵必须为消息队列提供服务并有效地处理返回的消息；如果队列已满，消息将被丢弃。

SDK 文件夹内容包括

- LeapC API 头文件
- lib — 构建 LeapC 库文件和 CMake 配置
- 示例— 包含用 C 编写的示例应用程序的 CMake 项目

这些的位置取决于使用的操作系统：

### 共享库

|OS|路径|
|---|---|
|Windows|`C:Program FilesUltraleapLeapSDKlibd`|
|Ubuntu|`/usr/lib/ultraleap-hand-tracking-service`|
|MacOS|`/Applications/Ultraleap Hand Tracking Service.app/Contents/LeapSDK/lib`|

### 头文件

|OS|路径|
|---|---|
|Windows|`C:Program FilesUltraleapLeapSDKinclude`|
|Ubuntu|`/usr/include`|
|MacOS|`/Applications/Ultraleap Hand Tracking Service.app/Contents/LeapSDK/include`|

### 示例

|OS|路径|
|---|---|
|Windows|`C:Program FilesUltraleapLeapSDKsamples`|
|Ubuntu|`/usr/share/doc/ultraleap-hand-tracking-service/samples`|
|MacOS|	`/Applications/Ultraleap Hand Tracking Service.app/Contents/LeapSDK/samples`|

