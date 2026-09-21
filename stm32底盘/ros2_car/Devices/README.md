# stm32-hal-devices
适配 STM32 HAL 库的常用外设/传感器模块，提供统一的配置入口与简单的使用接口。

## 目录结构
- Encoder/：增量式编码器读取
- MPU6050/：MPU6050 驱动与姿态相关接口
- OLED/：I2C OLED 显示驱动
- config.h：统一配置与硬件映射

## 依赖
- STM32 HAL 库（CubeMX 生成工程）
- 对应外设初始化（I2C、TIM、GPIO 等）

## 快速开始
1. 将需要的模块目录复制到工程中，并加入编译。
2. 在工程中包含 `config.h`，按实际硬件修改宏定义与句柄映射。
3. 在应用层调用模块初始化与读取接口。

## 配置说明（config.h）
- 通过 `DEVICE_xxx` 宏控制模块使能。
- 将外设句柄映射到模块宏，例如：
	- `MPU6050_I2C` → `hi2c2`
	- `Encoder_Left/Encoder_Right` → 编码器 TIM 句柄
