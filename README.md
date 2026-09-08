# 快捷方式生成器 (QuickShortcut)

一款Android快捷方式生成工具，一键生成快递身份码桌面快捷方式，支持拼多多、淘宝等电商平台。

## 功能特性

-   **预设应用**：内置拼多多、淘宝身份码快捷方式
-   **自定义图标**：从相册选择自定义图标
-   **URL Scheme跳转**：支持通过URL Scheme直达目标页面
-   **一键生成**：快速创建桌面快捷方式
- ✨ **简洁界面**：Material Design风格，操作简单直观

## 支持的应用

| 应用 | 功能 | URL Scheme |
|------|------|------------|
| 拼多多 | 身份码 | `pinduoduo://com.xunmeng.pinduoduo/...` |
| 淘宝 | 身份码 | `taobao://m.taobao.com/tbopen/...` |
| 自定义 | 手动输入 | 支持任意URL Scheme或Activity |

## 安装说明

### 下载APK

1. 从Release页面下载最新版本的APK文件
2. 将APK传输到Android手机
3. 在手机上点击安装（需要允许"未知来源"安装）

### 从源码构建

```bash
# 克隆项目
git clone https://github.com/your-username/QuickShortcut.git

# 进入项目目录
cd QuickShortcut

# 使用Gradle构建
./gradlew assembleDebug

# APK输出路径
# app/build/outputs/apk/debug/app-debug.apk
```

## 使用说明

1. **打开应用**：点击桌面上的"快捷方式生成器"图标
2. **选择预设**：点击"拼多多"或"淘宝"按钮自动填入配置
3. **自定义图标**（可选）：点击"从相册选择图标"选择自定义图标
4. **生成快捷方式**：点击"生成桌面快捷方式"按钮
5. **完成**：在桌面找到生成的快捷方式，点击即可直达目标页面

## 技术栈

- **开发语言**：Kotlin
- **UI框架**：Android Views (XML布局)
- **最低SDK**：Android 8.0 (API 26)
- **目标SDK**：Android 15 (API 35)
- **构建工具**：Gradle 8.14
- **Android Gradle Plugin**：8.7.0

## 项目结构

```
QuickShortcut/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/quickshortcut/
│   │   │   │   └── MainActivity.kt          # 主界面逻辑
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   └── activity_main.xml    # 界面布局
│   │   │   │   ├── drawable/                # 图标资源
│   │   │   │   ├── mipmap-anydpi-v26/       # 自适应图标
│   │   │   │   ├── values/                  # 字符串、样式
│   │   │   │   └── xml/                     # 备份配置
│   │   │   └── AndroidManifest.xml          # 应用清单
│   │   └── build.gradle.kts                 # 模块构建脚本
│   └── proguard-rules.pro                   # 混淆规则
├── gradle/
│   └── wrapper/
│       └── gradle-wrapper.properties        # Gradle配置
├── build.gradle.kts                         # 项目构建脚本
├── settings.gradle.kts                      # 项目设置
├── gradle.properties                        # Gradle属性
└── local.properties                         # 本地SDK路径
```

## 开发环境要求

- Android Studio Hedgehog (2023.1.1) 或更高版本
- JDK 17
- Android SDK 35
- Gradle 8.14

## 常见问题

### Q: 为什么生成的快捷方式无法跳转？
A: 请确保目标应用已安装，并且URL Scheme或Activity配置正确。

### Q: 支持哪些Android版本？
A: 支持Android 8.0 (API 26) 及以上版本。

### Q: 如何添加其他应用的快捷方式？
A: 点击"自定义"按钮，手动输入目标应用的包名、Activity或URL Scheme。

## 作者

**秦源鑫**
- 学校：南京邮电大学通达学院
- GitHub：[@your-username](https://github.com/your-username)

## 致谢

- Powered by Mimo v2.5
- 感谢所有开源社区的贡献

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

---

**注意**：本应用仅供学习交流使用，请勿用于商业用途。