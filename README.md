# ACG525 FPGA 实时多音色电子琴

2026年11月3日更新。

## 最新文件下载

- [完整工程 piano_zhengshiban.rar](https://github.com/everlasting-lwy/piano_zhengshiban/releases/download/v2026.11.03/piano_zhengshiban.rar)
- [最新版作品报告 DOCX](https://github.com/everlasting-lwy/piano_zhengshiban/releases/download/v2026.11.03/FPGA_piano_report.docx)
- [承诺书 PDF](https://github.com/everlasting-lwy/piano_zhengshiban/releases/download/v2026.11.03/chengnuoshu.pdf)
- [查看本次发布及全部下载附件](https://github.com/everlasting-lwy/piano_zhengshiban/releases/tag/v2026.11.03)

三个附件均按本次提供的原文件上传，内容不变。报告和承诺书仅使用英文下载文件名以兼容GitHub。作品报告以本页独立下载的最新版为准。

文件存放在 Releases 页面的 Assets 区域。请下载上面的工程 RAR，不要把GitHub自动生成的 Source code 压缩包当作完整工程。

[测试与演示报告](FPGA电子琴测试与演示报告.docx)继续保留，用于接线核对、模块联动和演示参考。旧 ZIP 工程包和旧独立作品报告已从当前主分支文件列表移除，避免重复。Git提交历史保留恢复能力。

## 使用入口

下载RAR后使用支持RAR格式的软件解压，先看工程内README.md。

- 引脚表：docs/PINOUT.md
- 构建和运行：docs/BUILD_AND_RUN.md
- Gowin工程入口：piano.gprj
- 当前固件：impl/pnr/piano1101_sd_ssd1306.fs
- 手机APK：mobile/android/dist/PianoLink-piano1101-SD-v2.3.apk
- P18转换工具：tools/p18_tool.py

## 项目功能

工程提供18实体键、四声部、四音色、32路谐波分量、表情控制、混响/回声/合唱、双OLED与双编码器、超声演奏、电脑MIDI及手机联动。32路谐波分量不代表32个独立声部。音频使用ACG525板载WM8960，接线以工程内引脚表为准。

SD曲谱采用电脑转换并拷入P18、FPGA自主读曲与脱机跟弹；已放弃APP经蓝牙写入及删除SD歌曲的使用流程。现有APK如显示历史SD写入入口，请勿使用。P18用于目标键位引导，不存原始时值，不会自动演奏。

## 文件校验与许可

下载后可用[SHA256SUMS.txt](SHA256SUMS.txt)核对三份新附件及保留的测试报告。

提供的RAR内目录和文件按原样保留；最新版作品报告以本次独立附件为准。第三方许可证随工程保留，本次未为原始及第三方代码额外授予开源许可证。
