# STM32F407 Gateway System

## 项目简介

这是一个基于STM32F407ZGT6微控制器的网关系统项目，用于乌东德项目。该系统集成了多种通信接口，支持数据采集、处理和转发功能。

## 硬件平台

- **主控芯片**: STM32F407ZGT6
- **封装**: LQFP144
- **Flash**: 1024KB
- **RAM**: 128KB
- **CCM RAM**: 64KB
- **外部晶振**: 10MHz HSE

## 系统特性

- **实时操作系统**: FreeRTOS CMSIS-V2
- **多串口通信**: 支持5个UART/USART接口
  - USART1: PA9(TX), PA10(RX)
  - USART2: PA2(TX), PA3(RX)
  - UART4: PA0(TX), PA1(RX)
  - UART5: PC12(TX), PD2(RX)
  - USART6: PC6(TX), PC7(RX)
- **系统时钟**: 168MHz主频
- **中断优先级**: 支持多级中断优先级管理

## 项目结构

```
├── Core/                   # 核心代码目录
│   ├── Inc/               # 头文件
│   └── Src/               # 源文件
├── Drivers/               # STM32 HAL驱动库
├── Middlewares/           # 中间件（FreeRTOS等）
├── 2531Z_GateWay.ioc     # STM32CubeMX配置文件
├── STM32F407ZGTX_FLASH.ld # Flash链接脚本
├── STM32F407ZGTX_RAM.ld   # RAM链接脚本
└── .project              # STM32CubeIDE项目配置
```

## 开发环境

- **IDE**: STM32CubeIDE
- **配置工具**: STM32CubeMX 6.13.0
- **HAL库版本**: STM32Cube FW_F4 V1.28.2
- **编译器**: GCC ARM

## 编译说明

1. 使用STM32CubeIDE打开项目
2. 选择Debug或Release配置
3. 编译生成.elf/.bin/.hex文件

## 功能模块

### 阶段1: 基础框架搭建
- [x] STM32CubeMX基础配置
- [x] FreeRTOS集成
- [x] 多串口初始化
- [ ] 基础任务创建
- [ ] 系统监控任务

### 阶段2: 通信协议实现
- [ ] AT指令解析
- [ ] HTTP协议支持
- [ ] 数据包处理
- [ ] 错误处理机制

### 阶段3: 高级功能
- [ ] 数据缓存管理
- [ ] 网络连接管理
- [ ] 系统配置管理
- [ ] 日志记录功能

## 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开 Pull Request

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 联系方式

- 项目维护者: alexycy
- 邮箱: alex.ycy@qq.com

---

*本项目为乌东德项目的一部分，专注于构建稳定可靠的网关通信系统。*