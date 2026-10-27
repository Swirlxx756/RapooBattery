# RapooBattery —— TrafficMonitor 鼠标电量插件

**这是 [TrafficMonitor](https://github.com/zhongyang219/TrafficMonitor) 的插件，不能单独运行。** 装好后，TrafficMonitor 的任务栏窗口 / 主窗口里会多一项，显示雷柏 VT1 MAX 鼠标的电量百分比。

本仓库只提供编译好的 DLL，不含源码。

## 适用范围

| 项目 | 要求 |
| --- | --- |
| 宿主程序 | TrafficMonitor **64 位（x64）** 版，已在 V1.86 上测试 |
| 鼠标 | 雷柏 VT1 MAX（设备 ID `VID_24AE&PID_1444`） |
| 连接方式 | 2.4G 接收器或有线 |
| 系统 | Windows 10 / 11 64 位 |

其他型号的雷柏鼠标没有测试过，大概率读不到电量。32 位版 TrafficMonitor 加载不了这个 DLL。

## 安装

1. 先装好 TrafficMonitor（[官方下载](https://github.com/zhongyang219/TrafficMonitor/releases)），选 x64 版。
2. 从 [Releases](../../releases) 下载 `RapooBattery.dll`。
3. 把它放进 TrafficMonitor 目录下的 `plugins` 文件夹（没有就新建一个）：

   ```text
   TrafficMonitor\
   ├── TrafficMonitor.exe
   └── plugins\
       └── RapooBattery.dll
   ```

4. 退出并重新打开 TrafficMonitor。
5. 右键任务栏窗口 →「显示设置」，勾选鼠标电量这一项。在「选项 → 插件管理」里可以看到插件是否已加载。

## 说明

- 插件通过 Windows 的 HID 接口读取鼠标上报的电量，不改动鼠标的任何设置。
- 鼠标刚连上或长时间空闲时，可能要等它上报一次数据才会显示电量。
- 卸载：退出 TrafficMonitor，删掉 `plugins\RapooBattery.dll` 即可。

## 校验

```text
RapooBattery.dll  SHA-256
122fcd49354fcf9e76b7229a16ce481ae457e0528b0114c0368da4dddef66419
```

## 声明

个人业余作品，与雷柏（Rapoo）和 TrafficMonitor 作者均无关联。「雷柏」「Rapoo」「VT1 MAX」是各自权利人的商标，这里只用来说明适用设备。按现状提供，不保证适用于所有设备。
