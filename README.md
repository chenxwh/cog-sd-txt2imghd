# cog-sd-txt2imghd

Try Replicate web demo here: [![Replicate](https://replicate.com/cjwbw/stable-diffusion-high-resolution/badge)](https://replicate.com/cjwbw/stable-diffusion-high-resolution)

This is a Cog implementation of Detailed, higher-resolution images from Stable-Diffusion, originally implemented by @[jquesnelle](https://github.com/jquesnelle) [here](https://github.com/jquesnelle/txt2imghd/blob/master/txt2imghd.py). Additionally, safety checker is added.


txt2imghd is a port of the GOBIG mode from [progrockdiffusion](https://github.com/lowfuel/progrockdiffusion) applied to Stable Diffusion, with [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) as the upscaler. It creates detailed, higher-resolution images by first generating an image from a prompt, upscaling it, and then running img2img on smaller pieces of the upscaled image, and blending the result back into the original image.

txt2imghd with default settings has the same VRAM requirements as regular Stable Diffusion, although generation of the detailed images will take longer.


## Get started locally
Install [Cog](https://github.com/replicate/cog) if you haven't: 
`curl https://storage.googleapis.com/replicate-public/codespaces/install-cog.sh | bash`

1. Clone stanle-diffusion `git clone https://github.com/CompVis/stable-diffusion`
2. Put `cog.yaml` and `predict.py` in the root directory of `stable-diffusion` and download weights (as noted at the top of `predict.py`)
3. Generate high-resolution images with `cog predict --prompt <your_prompt>`
