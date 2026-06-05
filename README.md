# Clawd Mochi 🦀🤖

基于 **Clawd**（Claude Code 像素螃蟹吉祥物）的 ESP32 桌面伴侣。

原版项目：[yousifamanuel/clawd-mochi](https://github.com/yousifamanuel/clawd-mochi)

## ✨ 新增功能

在原版基础上新增了 **5 个可爱表情**：

| 表情 | 效果 | 动画 |
|------|------|------|
| 💕 Heart | 爱心眼 ♥ ♥ | 心跳跳动 |
| 😴 Sleepy | 困困眼 - - | 点头打瞌睡 + Zzz |
| ⭐ Star | 星星眼 ✦ ✦ | 闪烁发光 |
| 😮 Surprised | 大圆眼 O O | 弹出放大 |
| 🥰 Blush | 弯弯眼 ^ ^ + 腮红 | 害羞眨眼 |

## 硬件

| 零件 | 规格 | 参考价 |
|------|------|--------|
| ESP32-C3 Super Mini | WiFi 微控制器 | ~¥5 |
| ST7789 1.54" TFT | 240×240 SPI 彩屏 | ~¥8 |
| 杜邦线 ×8 | 8-10cm | ~¥1 |
| M2×6mm 螺丝 ×2 | 固定屏幕 | - |
| USB-C 线 | 供电 | - |
| 3D 打印外壳 | PLA/PETG | - |

**总计：~¥15-20**

## 接线

> ⚠️ VCC 只接 **3.3V**，不要接 5V！

| 屏幕引脚 | ESP32-C3 GPIO |
|----------|---------------|
| VCC | 3V3 |
| GND | GND |
| SDA | GPIO 10 (MOSI) |
| SCL | GPIO 8 (SCK) |
| RES | GPIO 2 |
| DC | GPIO 1 |
| CS | GPIO 4 |
| BL | GPIO 3 |

## 软件设置

1. 安装 [Arduino IDE 2.x](https://www.arduino.cc/en/software)
2. 添加 ESP32 开发板：`文件 → 首选项 → 附加开发板管理器URL`：
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```
3. 安装库：`Adafruit GFX Library` + `Adafruit ST7735 and ST7789 Library`
4. 开发板设置：
   - Board: `ESP32C3 Dev Module`
   - USB CDC On Boot: **Enabled**
   - CPU Frequency: 160 MHz
5. 打开 `clawd_mochi.ino`，上传！

## 使用

1. USB 供电，等 3 秒开机
2. 连 WiFi：`ClaWD-Mochi`，密码：`clawd1234`
3. 浏览器打开 `http://192.168.4.1`
4. 选择表情，享受！

## 网页控制器

- 9 个表情按钮：Normal / Squish / Heart / Sleepy / Star / Surprised / Blush / Claude Code / Canvas
- 速度调节：slow / normal / fast
- 背景色 / 画笔颜色自定义
- 画布模式：手机实时画图
- 终端模式：交互式终端

## License

MIT License（代码）+ CC BY-NC-SA 4.0（3D 模型和图片）
