# IST8310

iSentek IST8310 三轴磁力计驱动模块 / Driver module for iSentek IST8310 3-axis magnetometer

## 硬件需求 / Required Hardware

i2c\_ist8310, ist8310\_int, ist8310\_rst, ramfs

## 构造参数 / Constructor Arguments

* rotation:        {w: 1.0, x: 0.0, y: 0.0, z: 0.0}
* topic\_name:      "ist8310\_mag"
* task\_stack\_depth: 1536

## 依赖 / Depends

无（No dependencies）

## LibXR 2.0 静态装配

使用 xrobot 1.0.1 的 `module` / 有序 `args`；构造函数显式注入外设与服务，实例按依赖顺序创建。参数名和顺序以头文件中的构造函数为准，固件示例见 `User/RobotConfig/`。

保留 PLDX 控制、协议、超时与离线保护。 `OnMonitor()` 由生成的监控循环直接调用。
