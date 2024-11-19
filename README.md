
# Jab Detection and counting using yolo

This project uses yolov10 for the training.


## Installation

### Dataset 
For Augmentation install Albumentation.

```bash
  pip install albumentations
```
### Training
Clone the yolo repo to a location.
All the requirements given inside the yolo folder.
Navigate to the yolo folder and run the command.    

```bash
  git clone https://github.com/THU-MIG/yolov10.git
  cd yolov10
  pip install -r requirements.txt
```
For downloading the weight files or copy the code in the jupyter notebook and execute:
```bash
  run weights_download.py
```
After that install ultralytics:
```bash
  pip install ultralytics
```
### Count of Jabs
install pytesseract for counting of punches.
```bash
  pip install pytesseract
```

## Prediction
If requirements are already installed for the training directly run the command:
```bash
  git clone https://github.com/THU-MIG/yolov10.git
  cd yolov10
  pip install -r requirements.txt
```
For prediction run this command:
```bash
yolo predict model=/content/drive/MyDrive/punches/yolov10/runs/detect/train2/weights/best.pt source=/content/drive/MyDrive/punches/yolov10/test2.mp4 half conf=0.25 save=True
```
model:path for best saved model

source: path of video or image on which you want to prediction

conf: 0.25(default) choose smaller value if the video has too many small objects.

save: True 
 
 The results would be saved in:
 yolov10\runs\detect\predict
 
 For more predictions it will create new folders.
## Count Jabs
While running for the count and pytesseract is installed.

Ensure Tesseract is in your PATH, or provide the direct path here:
```bash
  pytesseract.pytesseract.tesseract_cmd = r'/bin/tesseract'
```