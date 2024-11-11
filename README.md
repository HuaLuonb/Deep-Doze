# Deep-Doze
# Screen Doze Manager 屏幕休眠管理器
## 功能概述
Screen Doze Manager 是一个专为 Android 系统开发的电源管理模块，用于节省电量。
开发语言:C++
## 主要特性

### 1. 双模式运行
- **正常模式（亮屏）**
  - 启用所有 CPU 核心
  - 恢复正常网络连接
  - 启用系统服务
  - 取消休眠状态

- **休眠模式（息屏）**
  - 智能控制 CPU 核心数量
  - 选择性网络访问控制
  - 优化系统服务状态
  - 启用深度休眠

### 2. CPU 管理
- 动态调节 CPU 核心数量
- 自定义休眠模式下的核心数量
- 保持系统核心稳定运行

### 3. 网络管理
- 应用级网络访问控制
- 灵活的白名单机制
- 智能网络规则管理

### 4. 系统服务优化
- 位置服务管理
- 蓝牙控制
- 移动数据管理
- 系统同步控制
- 屏幕亮度调节

## 配置指南

### 配置文件位置
/data/local/tmp/doze_config.txt

CPU 控制
max_cpu_cores=8 # 设备最大CPU核心数
doze_close_cores=6 # 休眠时关闭的核心数
功能开关
enable_network_control=true # 启用网络控制
enable_location=false # 休眠时保持位置服务
enable_bluetooth=false # 休眠时保持蓝牙
enable_wifi=true # 休眠时保持WiFi
enable_mobile_data=true # 休眠时保持移动数据
enable_sync=false # 休眠时保持同步
其他设置
screen_brightness=30 # 休眠时屏幕亮度
网络白名单（逗号分隔）
network_whitelist=com.android.phone,com.android.systemui,com.android.settings #这些包名为示例

