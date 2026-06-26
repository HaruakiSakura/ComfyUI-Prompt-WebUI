<div align="center">
  
### [🇨🇳 简体中文](README.md) | [🇺🇸 English](README_EN.md)

</div>

## 💡 概要说明
本项目旨在让你在 ComfyUI 中能够像在 WebUI 中一样便捷地编写提示词。

本项目从 [weilin9999/WeiLin-ComfyUI-prompt-all-in-one](https://github.com/weilin9999/WeiLin-ComfyUI-prompt-all-in-one) 分支修改而来。由于原作者已停止维护，且原版插件在 **ComfyUI Vue3 新版前端架构** 下存在严重的兼容性 Bug，本项目专门针对此问题进行了深度修复，延续该插件在 ComfyUI 新版本中的生命力。

如果这个修复版拯救了你的工作流，请点个 ⭐️ Star 支持一下！

## 🛠️ 核心修复 (Bug Fixes)
原版插件在 Vue3 架构下存在**恶性 Bug**：修改提示词后运行任务，数据会瞬间被旧缓存覆盖，导致提示词修改全部丢失。
* **修复方案**：本分支通过键盘事件模拟与底层 LiteGraph 数据穿透机制，彻底解决了数据覆盖问题，保证提示词精准下发。
* **开发辅助**：本修复工作由 Deepseek V4 Flash 提供文件结构分析 与 Gemini 3.1 Pro Preview 提供代码逻辑辅助完成。

## 📥 安装方法
1. 通过 Git 克隆这个项目：在 `ComfyUIcustom_nodes` 目录下打开终端并运行：
`git clone https://github.com/HaruakiSakura/ComfyUI-Prompt-WebUI.git`
2. 下载 `.zip` 文件并将其内容解压到你的 `ComfyUIcustom_nodes` 文件夹中。

## 📖 使用说明：Lora 提示词写法
本插件支持标准的 Lora 调用语法：
* **`<lora:模型名称:模型+CLIP强度>`**
  * 示例：`<lora:ABC:0.4>` 
  * 含义：代表 Lora `ABC` 的模型强度与 CLIP 强度均为 0.4。
* **`<lora:模型名称:模型强度:CLIP强度>`**
  * 示例：`<lora:ABC:0.8:0>` 
  * 含义：代表 Lora `ABC` 的模型强度为 0.8，CLIP 强度为 0。

## 🤝 鸣谢与声明
本项目遵循 **MIT 开源协议**。

特别感谢以下项目与作者的卓越贡献与辛苦移植：
* [WeiLin-ComfyUI-prompt-all-in-one](https://github.com/weilin9999/WeiLin-ComfyUI-prompt-all-in-one) (原移植作者 weilin9999)
* [sd-webui-prompt-all-in-one-app](https://github.com/Physton/sd-webui-prompt-all-in-one-app) (核心模块作者 Physton)
* [ComfyUI-Custom-Scripts](https://github.com/pythongosssss/ComfyUI-Custom-Scripts) (作者 pythongosssss)
* [comfyui-sixgod_prompt](https://github.com/thisjam/comfyui-sixgod_prompt) (作者 thisjam)