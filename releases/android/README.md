# Android Releases / 安卓安装包

This directory hosts versioned Android APK files for Field Session.

此目录用于管理 Field Session 各版本的 Android 安装包（APK）。

## Directory Structure / 目录结构

```
releases/android/
├── README.md             ← this file
├── latest.json           ← latest version metadata
├── v1.0.0/
│   ├── field-session-v1.0.0.apk
│   └── CHANGELOG.md      ← release notes for this version
├── v1.1.0/
│   ├── field-session-v1.1.0.apk
│   └── CHANGELOG.md
└── ...
```

## Version Naming Convention / 版本命名规范

- Use [Semantic Versioning](https://semver.org/): `vMAJOR.MINOR.PATCH`
- APK file name format: `field-session-v{version}.apk`
- Each version gets its own directory with a `CHANGELOG.md`

| Part | Increment When | 递增条件 |
|------|---------------|---------|
| MAJOR | Incompatible changes | 不兼容的重大变更 |
| MINOR | New features (backward compatible) | 新增功能（向后兼容） |
| PATCH | Bug fixes | 缺陷修复 |

## How to Add a New Release / 如何发布新版本

1. Create a version directory: `mkdir v1.x.x`
2. Copy the APK into the directory: `cp path/to/build.apk v1.x.x/field-session-v1.x.x.apk`
3. Write release notes in `v1.x.x/CHANGELOG.md`
4. Update `latest.json` with the new version info
5. Commit and push

## latest.json Schema / 格式说明

```json
{
  "version": "1.0.0",
  "versionCode": 1,
  "releaseDate": "2026-03-24",
  "apkUrl": "v1.0.0/field-session-v1.0.0.apk",
  "changelog": "Initial release / 首次发布",
  "minSdkVersion": 21
}
```
