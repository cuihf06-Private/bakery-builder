# 🍞 面包工坊 APK 自动构建

## 功能说明

这个 GitHub Actions workflow 会自动将 `index.html` 游戏打包成 Android APK。

## 触发方式

### 1. 自动触发
推送代码到 `main` 分支时自动构建：
```bash
git add .
git commit -m "update game"
git push origin main
```

### 2. 手动触发
1. 进入你的 GitHub 仓库
2. 点击 **Actions** 标签
3. 选择 **Build Bakery APK** workflow
4. 点击右侧 **Run workflow** 按钮
5. 点击绿色的 **Run workflow** 确认

## 下载 APK

构建完成后：
1. 进入 Actions 页面
2. 点击最新的构建记录
3. 在页面底部的 **Artifacts** 区域
4. 下载 `面包工坊-APK-xxx` 文件
5. 解压 ZIP 后得到 APK 文件

## APK 信息

- **应用名称**: 面包工坊
- **包名**: com.bakery
- **最低版本**: Android 5.0 (API 21)
- **目标版本**: Android 13 (API 33)
- **屏幕方向**: 横屏锁定
- **存储**: 支持本地存储（LocalStorage）

## 优化特性

✅ 使用 Gradle Wrapper 确保构建一致性  
✅ 启用 JavaScript 和 DOM 存储  
✅ 支持游戏数据持久化  
✅ 自动适配屏幕尺寸  
✅ 横屏锁定，优化游戏体验  
✅ 构建日志自动上传（失败时）  
✅ APK 保留 30 天  

## 安装 APK

1. 将 APK 传输到 Android 设备
2. 在设置中允许"安装未知来源的应用"
3. 点击 APK 文件安装
4. 享受游戏！

## 技术细节

- **Java**: 17 (Temurin)
- **Gradle**: 8.0
- **Android Gradle Plugin**: 8.1.4
- **Build Tools**: 33.0.2
- **AndroidX**: AppCompat 1.6.1

## 故障排查

如果构建失败：
1. 检查 Actions 日志中的错误信息
2. 下载 `build-logs` artifact 查看详细日志
3. 确保 `index.html` 存在且格式正确
4. 检查 GitHub Actions 配额是否充足

---

**维护者**: cuihf06 (cuihf06@gmail.com)
