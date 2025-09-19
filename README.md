mkdir -p docs configs demo

cat > README.md <<'EOF'
# 新华三杯 - 智能宿舍环境监测系统

## 项目简介
本项目旨在搭建一个 **智能宿舍环境监测系统**，通过 ESP32 采集温湿度等传感器数据，并通过 MQTT 上传到后端，最终在网页/图表中实时展示。项目聚焦于宿舍环境的智能化管理，具备学习价值和实际应用意义。

## MVP（最小可行产品）
- ESP32 采集温湿度数据（DHT11/DHT22/SHT30）
- 数据通过 Wi-Fi 上传到 MQTT broker
- Python 后端接收数据并存储到 CSV 文件
- 前端用命令行/简易网页展示实时数据
- 系统能连续运行 1 小时并稳定上传数据
- 提供演示视频和 GitHub 开源代码

## 8 周冲刺计划

### W1 - 环境搭建与规划
- 安装 Arduino IDE/PlatformIO、Python、MQTT
- 在 GitHub 建立仓库，写下 MVP 和周计划

### W2 - 本地 MQTT 测试
- 跑通 Python 发布/订阅脚本
- 提交 demo 脚本到 repo

### W3 - 设备端入门
- ESP32 读取温湿度并串口输出
- 上传代码和串口截图

### W4 - 设备 → MQTT → 后端
- ESP32 上传数据到 MQTT
- Python 后端接收并存 CSV
- 上传演示短视频

### W5 - 可视化展示
- Python 实时绘图 或 搭建简单网页
- 支持展示多次采样数据

### W6 - 稳定性优化
- 实现断网重连，避免数据丢失
- 在 README 写容错说明

### W7 - 材料准备
- 录制 2 分钟 demo 视频
- 完成 PPT/技术方案

### W8 - 冲刺与提交
- 完善 repo 文档（README、接线图）
- 模拟答辩与现场演示

---

## 项目结构（预期）
\`\`\`
iot-xinhua3-cup/
├─ device/        # ESP32 代码
│   └─ sensor_demo.ino
├─ backend/       # Python 后端
│   ├─ mqtt_sub.py
│   └─ visualize.py
├─ docs/          # 接线图、PPT、demo 视频
└─ README.md
\`\`\`

---

## 演示与材料要求
- **演示视频**：≤ 2 分钟，展示从采集 → 上传 → 展示的完整流程  
- **README**：包含接线图、运行步骤、依赖环境  
- **PPT**：简要介绍问题、方案、实现和成果  
- **代码**：能编译运行，有必要注释
EOF

# 创建占位文件（方便在网页中直接看到文件夹）
echo "占位文件 - docs" > docs/placeholder.md
echo "占位文件 - configs" > configs/placeholder.md
echo "占位文件 - demo" > demo/placeholder.md
