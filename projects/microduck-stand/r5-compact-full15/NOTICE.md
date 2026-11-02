# 来源、署名与许可说明

本目录整理自 Microduck_JIG190_R5_Compact_Full15，版本 R5.0-rc1；PDF、3MF、11 个 STL、工艺参数与两张 R5 CAD 渲染图保留源文件字节。本次增加分享目录、中文 README、来源映射及 SHA-256 清单，未修改模型几何。

## 来源

- Pollen Robotics 的 [microduck_rl](https://github.com/pollen-robotics/microduck_rl) 与 [microduck](https://github.com/pollen-robotics/microduck)：机器人机械外形、关节模型和运行时参考。
- fanhao375 的 [microduck-replica](https://github.com/fanhao375/microduck-replica)：复刻硬件、外壳与 IMU PCB 参考；独立六面盒按参考 PCB 的名义几何设计，实际变体需重新核对。
- superobk 的 [microduck-imu](https://github.com/superobk/microduck-imu)、[microduck](https://github.com/superobk/microduck) 和 [microduck-lab](https://github.com/superobk/microduck-lab)：源包软件与课程参考。该打印分享目录不包含校准软件或源码快照。
- ROBOTIS 文档及 Pollen Robotics 的 rustypot：源包中的舵机参考。

已知锁定版本保留于 [sources.lock.json](docs/sources.lock.json)。源包中的完整软件快照 / 来源清单不随本目录发布。本目录的 MANIFEST 只记录实际导入文件，不声称包含完整设计复现链。

## 模型及图片许可

Pollen Robotics 机器人模型原说明见 [LICENSE-MODELS-UPSTREAM.md](docs/LICENSE-MODELS-UPSTREAM.md)，其指定模型采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)。源包 PDF 中保留的 R4 机器人姿态参考图按该许可署名，仅帮助识别姿态，不是 R5 配合验证证据。原始机器人 STL 未在本目录重新分发。

根目录 MIT LICENSE 不替代第三方模型、图片和派生材料的许可或作者署名。该上游模型许可文件的覆盖范围按其原文理解，不将其自动扩展为所有独立夹具文件的统一许可。独立 R5 夹具的源包没有单列模型许可；再分发或其他使用方式需要明确许可时，应向维护者确认。

## 状态与名称

这是独立的数字样机与打印准备资料，不是 Pollen Robotics、ROBOTIS、STMicroelectronics 或 Bambu Lab 发布或认证的产品。相关商标仅用于识别适配对象。R5 渲染图来自新工装 CAD；未完成完整机器人干涉、实际切片、实物受力与精度验收。
