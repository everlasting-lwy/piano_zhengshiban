# ACG525 FPGA 实时多音色电子琴

正式整理版，2026年11月2日。完整工程以压缩包交付，保留全部目录结构。

## 下载

- [完整工程 piano_zhengshiban.zip](piano_zhengshiban.zip)（打开后点 Download raw 下载并解压）
- [作品报告](FPGA实时多音色电子琴作品报告.docx)
- [测试与演示报告](FPGA电子琴测试与演示报告.docx)

## 工程内容

包含373个文件：Gowin工程、RTL源码、约束、ROM、当前固件、Android源码与APK、Windows MIDI可视化工具、P18转换工具、测试样本、验证记录和两份最新报告。历史存档、签名密钥、临时缓存和未完成的P18桌面转换器草稿不包含在内。压缩包内SHA256.json可校验各文件。

## 当前功能

18实体键（C4～F5）、四声部、四音色、32路谐波分量、三表情调节、混响/回声/合唱、双OLED与双编码器、超声演奏、电脑MIDI、手机36键联弹、曲库、离线音频转谱、下落练习、整曲RAM引导下载，以及SD卡自主读曲与脱机跟弹。32路谐波分量不代表32个独立声部。

音频采用ACG525板载WM8960左声道扬声器；旧MAX98357A和陶晶驰串口屏不使用。SD使用电脑转换/拷入P18，已放弃通过APP蓝牙写入和删除SD歌曲；现有APK保留的历史入口不要操作。P18用于按键引导，不会自动演奏。

## 解压后先看

- README.md：工程入口及范围说明
- docs/PINOUT.md：完整接线表
- docs/BUILD_AND_RUN.md：构建、下载与使用
- piano.gprj / build.tcl：Gowin工程与构建脚本
- impl/pnr/piano1101_sd_ssd1306.fs：当前发布固件
- mobile/android/dist/PianoLink-piano1101-SD-v2.3.apk：手机安装包
- tools/p18_tool.py：已验证的CSV转P18命令行工具

工程内部文件名保留piano1101，避免破坏引用。未更改硬件代码及已发布程序。Android签名密钥仅保留本机，重新生成签名的APK不能直接覆盖原签名版本。未为原始及第三方代码额外授予开源许可证，第三方许可证保留在工程内。

## 压缩包校验

SHA256：`2dc3db21bcac5973fde4dc426a9c95a2b8bf736e9d36dd1243966114daa9f283`
