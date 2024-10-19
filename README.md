## comfy
Get the ComfyUI windows portable 7z:
### [Download Portal](https://github.com/calcuis/comfy/releases/download/0.0.2/ComfyUI_windows_portable.7z)
- decompress the 7z bundle file: Extract All... (it includes everything you need)
- setup: pull any checkpoint (sample [here](https://huggingface.co/calcuis/ckpt/tree/main)) file (.ckpt/.safetensors) into the folder ./ComfyUI/models/checkpoints
- go back to the main directory; look for run_cpu or run_gpu
- run the Batch file (.bat)

![screenshot](comfy.png)

#### GGUF-supported upgrade
Run gguf model (flux1 as an example below):
- download [flux1-dev-Q4_0.gguf](https://huggingface.co/city96/FLUX.1-dev-gguf/blob/main/flux1-dev-Q4_0.gguf) (6.32GB); pull it to ./ComfyUI/models/unet
- download [clip_l.safetensors](https://huggingface.co/comfyanonymous/flux_text_encoders/blob/main/clip_l.safetensors) (234MB) and [t5xxl_fp8_e4m3fn.safetensors](https://huggingface.co/comfyanonymous/flux_text_encoders/blob/main/t5xxl_fp8_e4m3fn.safetensors) (4.55GB); pull them to ./ComfyUI/models/clip
- download [ae.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-schnell/blob/main/ae.safetensors) (319MB); pull it to ./ComfyUI/models/vae
- run the .bat file under the main directory (it will activate the py backend as well as the js frontend)
- drag [workflow-gguf.json](https://github.com/calcuis/comfy/blob/main/workflow-gguf.json) to the activated browser

![screenshot](gguf.png)
