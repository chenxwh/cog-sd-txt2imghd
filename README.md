# cog-sd-txt2imghd

This is a Cog implementation of Detailed, higher-resolution images from Stable-Diffusion, originally implemented by @[jquesnelle](https://github.com/jquesnelle) at https://github.com/jquesnelle/txt2imghd/blob/master/txt2imghd.py


txt2imghd is a port of the GOBIG mode from [progrockdiffusion](https://github.com/lowfuel/progrockdiffusion) applied to Stable Diffusion, with [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) as the upscaler. It creates detailed, higher-resolution images by first generating an image from a prompt, upscaling it, and then running img2img on smaller pieces of the upscaled image, and blending the result back into the original image.

txt2imghd with default settings has the same VRAM requirements as regular Stable Diffusion, although generation of the detailed images will take longer.
