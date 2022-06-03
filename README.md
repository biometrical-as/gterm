
# ViTerm 
<p align="center">
  <img src="/figures/viterm_logo.png" alt="Viterm logo"/>
</p>

Displays video, images, webcam or rtsp stream in terminal. 

## Setup
```
pip install -r requirements.txt
```

## Use
```
python viterm.py <media> -r <Height Width> -c <display character> 
```
* media: Accepts video, images, webcam-index, rtsp-streams and anything else which is supported by cv2.VideoCapture
* --resolution: Two values. Int to set pixel width/height, float to scale image dimension. The image is scaled down to a width of 40 by default (keeping aspect ratio)
* --character: String of what character to use as a display-pixel. Default is ██. 
