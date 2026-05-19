# esp32-mcp-parenting-robot
An open-source parenting &amp; educational robot powered by ESP32 with MCP protocol support, including firmware, server-side OS, and 3D-printable enclosure files.
# esp32-mcp-parenting-robot

> 一款基于 ESP32-S3/C3 主控开发、支持 MCP 协议的开源育儿教育机器人方案，包含固件、云机器人大脑系统、可 3D 打印外壳文件与组装指南。
> 
> An open-source parenting & educational robot powered by ESP32-S3/C3 with native MCP protocol support, including pre-built firmware, cloud-based robot brain, 3D-printable enclosure files and assembly guides.

---

## ✨ 项目最大亮点：自主开发的云机器人大脑控制操作系统
## ✨ Project Highlight: Custom Cloud Robot Brain Control OS

本项目最核心的优势，是一套完全自主开发的**云机器人大脑控制操作系统**，专为育儿教育场景打造：
The core innovation of this project is a fully custom **cloud-based robot brain control OS**, built specifically for parenting & education scenarios:

- 固件原生集成 **MCP 协议调用**，对接 Wowing Ai Lab 云服务器的机器人大脑系统，内置主流 MCP 中转站，**无需手动桥接本地部署 MCP 协议，真正实现开机即用**。
- Native MCP protocol integration in firmware connects directly to the Wowing Ai Lab cloud robot brain system, with built-in MCP relays — **no local MCP bridging required, just power on and use**.

- 烧录后即可通过 **PWA 手机网页** 自由控制机器人的姓名、性格、语音音色，实现高度个性化定制。
- After flashing, you can fully customize the robot’s name, personality and voice via the **mobile PWA web interface**.

- 原生支持 **图片分析功能**（如作业批改）：机器人可随时随地将拍摄的图片上传云端分析，解码成结构化知识内容，并同步到对话上下文，让机器人能基于图片内容进行深度对话。
- Native **image analysis support** (e.g., homework grading): The robot uploads captured images to the cloud for analysis, decodes them into structured knowledge, and syncs to conversation context for deep, context-aware dialogue.

- MCP 协议作为扩展能力正在持续更新，目前已支持：必应搜索、大师思维模式、中国紫薇算命等功能，启动对应服务即可一键写入机器人云大脑，无需修改固件。
- MCP-based extensions are continuously being added, including Bing Search, Master Thinking Mode, and Chinese Zi Wei Fortune Telling — enable services to push updates to the cloud brain without re-flashing firmware.

---

## 🛠️ 硬件与开发环境
## 🛠️ Hardware & Development

| 中文说明 | English Description |
| :--- | :--- |
| 主控方案：**ESP32-S3（主力）/ ESP32-C3（可选）**，原生支持 WiFi 无线通信 | MCU: **ESP32-S3 (main) / ESP32-C3 (optional)** with native WiFi support |
| 屏幕：0.96 寸 I2C OLED (128×64) | Display: 0.96" I2C OLED (128×64) |
| 电源：Type-C 接口 + 可充电锂电池 | Power: Type-C interface + rechargeable Li-ion battery |
| 烧录工具：使用 **Flash Download Tool 一键烧录**，无需复杂开发环境配置 | Flashing: **One-click flash via Flash Download Tool**, no complex dev environment needed |

---

## 🚀 快速上手指南
## 🚀 Quick Start Guide

### 1. 3D 打印外壳
### 1. 3D Print the Enclosure
- 使用 `3D Printing Files for Enclosure/` 目录下的文件打印外壳，推荐材料 PETG，填充率 20%。
- Print the enclosure using the files in the `3D Printing Files for Enclosure/` directory. Recommended material: PETG, infill 20%.

### 2. 硬件组装
### 2. Hardware Assembly
- 按 `Electronic Components Purchase Instructions/` 中的文档焊接与组装所有配件，注意电源正负极与主控引脚定义。
- Solder and assemble all components following the docs in `Electronic Components Purchase Instructions/`. Pay attention to power polarity and MCU pin definitions.

### 3. 固件一键烧录
### 3. One-Click Firmware Flash
1. 下载 `wowing-esp32固件BIN/` 目录下的预编译 `.bin` 固件文件
2. 安装并打开 **Flash Download Tool**
3. 选择对应主控型号，加载固件文件，配置串口与烧录地址
4. 点击「Start」即可一键烧录，无需额外开发环境

1. Download the pre-compiled `.bin` firmware from `wowing-esp32固件BIN/`
2. Install and open **Flash Download Tool**
3. Select your MCU model, load the firmware file, configure serial port and flash address
4. Click “Start” to flash — no extra dev environment required

### 4. 云大脑配置与使用
### 4. Cloud Brain Setup & Usage
1. 烧录完成后，机器人开机自动连接预设 WiFi
2. 手机打开项目配套的 PWA 网页，绑定机器人设备
3. 即可在网页端设置机器人姓名、性格、语音，开启图片分析、MCP 扩展功能
4. 新增的 MCP 服务（如搜索、算命等）启动后，将自动同步到机器人云大脑，无需重复烧录

1. After flashing, the robot will connect to the configured WiFi automatically
2. Open the project PWA web page on your phone and bind the robot device
3. Set the robot’s name, personality, voice, and enable image analysis / MCP extensions via the web interface
4. New MCP services (search, fortune-telling, etc.) will sync to the cloud brain automatically — no re-flashing needed

---

## 📂 项目结构
## 📂 Project Structure

esp32-mcp-parenting-robot/
├── 3D Printing Files for Enclosure/ # 外壳 3D 打印文件（STL 格式）
│ └── [模型文件].stl # 机器人主体、配件外壳模型
│
├── Electronic Components Purchase Instructions/ # 电子元器件采购说明
│ └── hardware-list.md # 完整采购清单与购买渠道参考
│
└── wowing-esp32 固件 BIN/ # ESP32-S3/C3 预编译固件
└── factory_firmware.bin # 支持 Flash Download Tool 一键烧录


---

## 📄 License
本项目采用 **MIT License** 开源，详见 [LICENSE](LICENSE) 文件。

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
