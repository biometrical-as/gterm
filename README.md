
# ViTerm 
<p align="center">
  <img src="/figures/viterm_logo.png" alt="Viterm logo"/>
</p>

Displays video, images, webcam or rtsp stream in terminal. 

## Requirements
viterm is developed for python >=3.8.

## Setup
```
pip install -r requirements.txt
```

### Optional
To make an alias, append the following line to your .bashrc (linux) or .zshrc (mac):

```bash
viterm() { python <path to viterm.py> "$@" ;}
```

If you want it to run in a specific conda environment, add the following instead:

```bash
viterm() { conda run -n <your environment name> python <path to viterm.py> "$@" ;}
```

Run ```source ~/.bashrc``` (linux) or ```source ~/.zshrc``` (mac). You can now call viterm in your terminal with ```viterm```

## Use
Without alias:
```bash
python viterm.py <media> -r <Height Width> -c <display character> 
```
With alias:
```bash
viterm <media> -r <Height Width> -c <display character> 
```
* media: Accepts video, images, webcam-index, rtsp-streams and anything else which is supported by cv2.VideoCapture
* --resolution: Two values. Int to set pixel width/height, float to scale image dimension. The image is scaled down to a width of 40 by default (keeping aspect ratio)
* --character: String of what character to use as a display-pixel. Default is ██. 
