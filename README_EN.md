<div align="center">
  
### [🇨🇳 简体中文](README.md) | [🇺🇸 English](README_EN.md)

</div>

## 💡 Overview
This project aims to let you write prompts in ComfyUI as conveniently as you do in WebUI.

This project is a modified branch of [weilin9999/WeiLin-ComfyUI-prompt-all-in-one](https://github.com/weilin9999/WeiLin-ComfyUI-prompt-all-in-one). Since the original author has stopped maintaining it, and the original plugin has a severe compatibility bug under the **new ComfyUI Vue3 front-end architecture**, this project specifically addresses and fixes this issue, extending the plugin's lifespan in newer versions of ComfyUI.

If this fixed version saves your workflow, please consider giving it a ⭐️ Star!

## 🛠️ Bug Fixes
The original plugin had a **critical bug** under the Vue3 architecture: after modifying the prompt and running a task, the data would be instantly overwritten by the old cache, causing all prompt modifications to be completely lost.
* **Fix Solution**: This branch thoroughly resolves the data overwrite issue through keyboard event simulation and a low-level LiteGraph data penetration mechanism, ensuring prompts are dispatched accurately.
* **Development Assistance**: This fix was completed with file structure analysis provided by Deepseek V4 Flash and code logic assistance from Gemini 3.1 Pro Preview.

## 📥 Installation
1. Clone this project via Git: Open your terminal in the `ComfyUI\custom_nodes` directory and run:
   `git clone https://github.com/HaruakiSakura/ComfyUI-Prompt-WebUI.git`
2. **Alternatively**, download the `.zip` file and extract its contents into your `ComfyUI\custom_nodes` folder.

Restart ComfyUI to take effect.

## 📖 Usage: Lora Prompt Syntax
This plugin supports standard Lora invocation syntax:
* **`<lora:model_name:model+clip_weight>`**
  * Example: `<lora:ABC:0.4>` 
  * Meaning: Sets both the model weight and CLIP weight for Lora `ABC` to 0.4.
* **`<lora:model_name:model_weight:clip_weight>`**
  * Example: `<lora:ABC:0.8:0>` 
  * Meaning: Sets the model weight to 0.8 and the CLIP weight to 0 for Lora `ABC`.

## 🤝 Credits & Acknowledgements
This project is licensed under the **MIT License**.

Special thanks to the following projects and authors for their outstanding contributions and hard work:
* [WeiLin-ComfyUI-prompt-all-in-one](https://github.com/weilin9999/WeiLin-ComfyUI-prompt-all-in-one) (Original port author: weilin9999)
* [sd-webui-prompt-all-in-one-app](https://github.com/Physton/sd-webui-prompt-all-in-one-app) (Core module author: Physton)
* [ComfyUI-Custom-Scripts](https://github.com/pythongosssss/ComfyUI-Custom-Scripts) (Author: pythongosssss)
* [comfyui-sixgod_prompt](https://github.com/thisjam/comfyui-sixgod_prompt) (Author: thisjam)