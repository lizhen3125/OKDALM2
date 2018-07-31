## 1.1 (2018/07/31)
### Enhancements
- 增加 -l 对输出 mavenLocal 的支持
- 增加配置 module 的发布类型
  - 可单独配置 module 的 MavenType、ArtifactId、GroupId
  - eg. LibAMavenType = release
- 遍历 Module 依赖时，过滤 lint-gradle 依赖
- 增加 -i >>> --info --stacktrace

### Bug Fixes
- 修复更新 module 信息时出现正则误匹配
  - eg. AModule 、AAModule，当修改 AModule 时，AAModule 误修改

### Changes
- 配置 -u 时改为强制升级，无论当前是 snapshot 还是 release
- 配置 -r 时改为强制设置 release，并重写 version_properties.gradle 中的配置，优先于 -u
- deploy mode 默认为 -a
  - python deploy.py [-a]
- 移除 artifactory.gradle 中 android 的判断

## 1.0 
  fork from https://github.com/luckybilly/OKDALM 