# stm32-learning

STM32 嵌入式学习项目仓库 —— 基于 **STM32F103** 开发板。

## 硬件

| 项目 | 型号 |
|------|------|
| MCU | STM32F103（具体型号待板子到货确认） |
| 开发板 | （待确认：江协最小系统 / 正点原子战舰 / Blue Pill） |
| 调试器 | ST-Link V2 |
| 串口 | CH340 USB转串口 |

## 环境

- IDE: Keil MDK-Arm v5.24a
- 路径: `F:\Tools\MDK5\Keil_v5`
- 器件包: Keil.STM32F1xx_DFP.2.2.0
- 库版本: 标准外设库 (Standard Peripheral Library)
- 编译器: ARM Compiler v5.x (MDK自带)

## 目录结构

```
led-blink/
├── src/              # 源代码
│   ├── main.c        # 主程序入口
│   ├── startup_*.s   # 启动文件
│   └── *.c           # 外设驱动/模块
├── inc/              # 头文件
├── lib/              # 标准库文件
├── .gitignore        # Git 忽略规则
└── README.md         # 本文件
```

## 快速开始

1. 用 MDK 打开工程 `.uvprojx` 文件
2. 在 `Options for Target` → `C/C++` → Define 中确认宏定义：
   - `USE_STDPERIPH_DRIVER,STM32F10X_MD` (C8T6) 或
   - `USE_STDPERIPH_DRIVER,STM32F10X_HD` (ZET6)
3. 按 F7 编译 → Ctrl+F5 下载到开发板

## 学习路线

- [x] GPIO 输出（LED 闪烁）
- [ ] GPIO 输入（按键）
- [ ] 中断与外部中断 EXTI
- [ ] 定时器 TIM
- [] PWM 输出
- [ ] UART 串口通信
- [ ] I2C / SPI 传感器驱动
- [ ] OLED 显示屏
- [ ] FreeRTOS 多任务
- [ ] MQTT 上云（综合项目）

## License

MIT License

## Author

**Huang Bi** (毕黄)  
物联网工程专业 / 大四学生
