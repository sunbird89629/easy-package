# easy-package

> 一个简易的 Android APK 打包 GUI 工具。

> **⚠️ Status: Archived (2020-04)**
> This project is archived and no longer maintained. Modern Android build workflows have moved to Gradle-based CI (Fastlane, GitHub Actions, Bitrise, etc.), which cover this tool's use cases more robustly. See [Alternatives](#alternatives) below.

---

**Language**: [English](#english) · [简体中文](#简体中文)

---

## Screenshots

<!-- Screenshots removed with archive; refer to the source for the original UI. -->

## English

### What it was

`easy-package` was a lightweight desktop app to help Android developers package APK builds without touching Gradle commandline — pick a project, tweak parameters, and click "package". Useful in the pre-CI era when many teams built APKs on individual dev machines.

### Why it's archived

- **Android Gradle Plugin evolved** — the assumptions this tool made about build scripts no longer hold in AGP 7+
- **CI became standard** — teams now build on Fastlane / GitHub Actions / Bitrise / self-hosted runners
- **My focus shifted** — moved from Android native to Flutter tooling (`http_inspector`, `flutter_ci_tools`, etc.)

### Alternatives

For modern Android release workflows:

| Need | Recommendation |
|---|---|
| Cloud CI | [GitHub Actions](https://github.com/features/actions) with `gradle build` |
| Local automation | [Fastlane](https://fastlane.tools/) `gradle` action |
| Multi-flavor builds | `./gradlew assemble<Flavor><BuildType>` + Fastlane matrices |
| Signing management | [Fastlane match](https://docs.fastlane.tools/actions/match/) or `signingConfigs` in Gradle |

For **Flutter** projects specifically, see my newer maintained tool: [**flutter_ci_tools**](https://github.com/sunbird89629/flutter_ci_tools).

### License

See [LICENSE](LICENSE).

---

## 简体中文

### 这是什么

`easy-package` 是一个轻量级桌面工具，让 Android 开发者不用敲 Gradle 命令就能打 APK —— 选个项目、调参数、点"打包"。在 CI 还没普及的年代，是很多团队用来在开发者电脑上出 APK 的方案。

### 为什么归档

- **Android Gradle Plugin 大变** —— 工具原本假设的构建脚本结构在 AGP 7+ 之后已经不成立
- **CI 成为标配** —— 主流团队现在都用 Fastlane / GitHub Actions / Bitrise 打包
- **我的重心变了** —— 已经从 Android 原生转向 Flutter 工具链（[http_inspector](https://github.com/sunbird89629/http_inspector) / [flutter_ci_tools](https://github.com/sunbird89629/flutter_ci_tools) 等）

### 现代替代方案

| 需求 | 推荐工具 |
|---|---|
| 云端 CI | GitHub Actions + `gradle build` |
| 本地自动化 | [Fastlane](https://fastlane.tools/) `gradle` action |
| 多渠道打包 | `./gradlew assemble<Flavor><BuildType>` + Fastlane 矩阵 |
| 签名管理 | Fastlane match 或 Gradle 的 `signingConfigs` |

Flutter 项目请看我在维护的：[**flutter_ci_tools**](https://github.com/sunbird89629/flutter_ci_tools)。

### 感谢

感谢当年 6 位 star 这个项目的朋友 —— 说明这个方向的痛点是真实存在的，只是解决方式随时代进化了。

### 协议

见 [LICENSE](LICENSE)。
