# Player-detection-and-tracking-using-Yolov4
The following code uses YOLOv4, Deepsort and Tensorflow to implement object detection and tracking on mp4 format videos. Additionally, you can select a particular player, drop the rest and track him only for the rest of the video. The output is a .avi format video, with detection and tracking performed on it.

# How it works
Prerequisites:
- You need python 3.7 to be able to install the Tensorflow version used in this program.
- Make sure your GPU is disabled, this modification works on CPU only.

To run this code, clone it your local machine and unzip the folder.
On your command prompt, run the following commands:
- pip install -r requirements.txt
- python save_model.py --model yolov4 
- python object_tracker.py --video ./data/video/inputvideo.mp4 --output ./outputs/output.avi --model yolov4
(replace inputvideo.mp4 with the name of your input video, and  output.avi with the name you wish to give your output video)

Make sure to upload your input video in the following folder:
data > video
Your output video will be saved in the outputs folder.

# Acknowledgments
This code is an extension on the following git repository, https://github.com/theAIGuysCode/yolov4-deepsort.

# Improvements
Although the code works fine otherwise, when a particular player detection (say P) is lost, its assigned a new tracking ID once gained back. If you are tracking player P, you wil notice that its bounding box disappears at the instant, its detection is lost. To regain tracking, click on the player again, and the bounding box shall reappear.
