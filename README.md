# STM32 学习笔记与实验工程 🚀

本项目记录了我在大二年级下学期进行 STM32 开发的学习过程。主要基于 **STM32CubeMX** 配置与 **Keil MDK** 开发环境。

## 🛠 开发环境
- **硬件平台**: STM32F103ZET6 开发板 
- **配置工具**: STM32CubeMX
- **IDE**: Keil uVision5 (MDK-ARM)
- **烧录硬件**: USB线 连接板载 CH340 (USB-to-UART)
- **烧录软件**: FlyMcu
- **代码规范**: HAL 库 (Hardware Abstraction Layer)

## 📁 仓库结构说明
- `MDK-ARM/`: Keil 工程文件夹，存放启动文件与编译配置。
- `Core/Src/`: 核心源代码（main.c, stm32f1xx_it.c 等）。
- `Core/Inc/`: 对应的头文件。
- `Drivers/`: STM32 HAL 库文件及 CMSIS 驱动。
- `*.ioc`: CubeMX 配置文件（**修改引脚配置请打开此文件**）。

## 📝 已实现功能清单
- [x] **LED_Blink**: 基础 GPIO 控制，实现 LED 闪烁。
- [x] **UART_Debug**: 串口通讯，实现 printf 重定向调试。
- [ ] **Timer_PWM**: 定时器产生 PWM 波控制舵机或电机。
- [ ] **ADC_DMA**: 多通道 ADC 采集，配合 DMA 降低 CPU 占用。
- [ ] **FreeRTOS**: (计划中) 嵌入式实时操作系统移植。

## 🚀 如何运行
1. 确保已安装 **Keil MDK** 及对应的 **STM32 Pack** 包。
2. 双击 `MDK-ARM/` 文件夹下的 `.uvprojx` 文件打开工程。
3. 在 Keil 中点击 `Build` (F7) 进行编译。
4. 连接好开发板，点击 `Download` (F8) 烧录程序。

## 📌 注意事项
- 本工程已配置 `.gitignore`，自动忽略了编译生成的 `Objects/` 和 `Listings/` 文件夹，保持仓库纯净。

---
Created by [Liyangchen-dev](https://github.com/Liyangchen-dev)