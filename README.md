# Vehicle-Counting-System

### Steps to run Code
- Clone the repository.
```
git clone https://github.com/RizwanMunawar/yolov7-object-tracking.git
```
- Goto the cloned folder.
```
cd Vehicle-Counting-System
```
- Create a virtual envirnoment (Recommended, If you dont want to disturb python packages)
```
### For Linux Users
python3 -m venv Vehicle-Counting-System
source Vehicle-Counting-System/bin/activate

### For Window Users
python3 -m venv Vehicle-Counting-System
cd Vehicle-Counting-System
cd Scripts
activate
cd ..
cd ..
```
- Upgrade pip with mentioned command below.
```
pip install --upgrade pip
```
- Install requirements with mentioned command below.
```
pip install -r requirements.txt
```
- Run the code with mentioned command below (by default, pretrained [yolov7](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt) weights will be automatically downloaded into the working directory if they don't already exist).
```
# for detection only
python detect.py --weights yolov7.pt --source "your video.mp4"

#if you want to change source file
python detect_and_track.py --weights yolov7.pt --source "your video.mp4"

#for specific class (person)
python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --classes 0

#for colored tracks 
python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --colored-trk

#for saving tracks centroid, track id and bbox coordinates
python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --save-txt --save-bbox-dim
```

- Output file will be created in the ```working-dir/runs/detect/obj-tracking``` with original filename




 ### References
 - https://github.com/WongKinYiu/yolov7
 - https://github.com/abewley/sort
 - https://github.com/RizwanMunawar
