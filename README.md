# CUP and DISC segmentation using YOLO V5 instance Segmentation

<img src= "https://github.com/gSayak/cup-disc-Segmentation/blob/main/assets/Blank%204%20Grids%20Collage.png"></img>

This repo uses YoloV5 for detection of cup and disc from fundus image. 
# What is Cup and Disc
In ophthalmology, the cup and disc refer to the optic nerve head and surrounding retina in the back of the eye. The cup is the center of the optic nerve head, while the disc is the surrounding tissue. The relationship between the size of the cup and disc can provide important information for diagnosing and monitoring certain eye conditions, such as glaucoma.

Doctors often use fundus imaging, a non-invasive imaging technique that captures detailed images of the retina, to assess the cup-to-disc ratio (CDR). A high CDR can indicate glaucoma or other optic nerve disorders, which can cause vision loss if not detected and treated early.

However, the process of manually analyzing fundus images to measure the CDR can be time-consuming and prone to human error. This is where automated segmentation algorithms like Mask R-CNN, YoloV5 and YoloV7 can be useful, as they can accurately and efficiently segment the cup and disc in fundus images, enabling faster and more reliable diagnosis of eye diseases.

# Dataset
This repo has been trained on the RIM-ONE dataset. RIM-ONE DL is a unified retinal image database for assessing glaucoma using Deep Learning. The full paper is available in this publication of the Image Analysis and Stereology journal: https://www.ias-iss.org/ojs/IAS/article/view/2346

The directory structure followed is:
<img src="https://github.com/gSayak/cup-disc-Segmentation/blob/main/assets/dataset.jpg"></img>

  The repo was annotated manually using <a href="https://roboflow.com/">RoboFlow</a>
  
# Steps to run segmentation on a Fundus image
For running this repo on Google Colab you will need to 
1. Clone the repo 
2. Upload the <a href="ttps://github.com/gSayak/cup-disc-Segmentation/blob/main/test_yolov5_segmentation.ipynb">test_yolov5_segmentation.ipynb</a> in a google drive
3. Open the test_yolov5_segmentation.ipynb with Google Colab
4. Once the file gets opened in Colab, upload the fundus image you want to mask in Google colab either by using the upload button or by simple drag and drop
5. Copy the path of the fundus image that you uploaded and replace the `'path to/fundus.jpg` with the path you copied in the earlier step
```bash
!python segment/predict.py --img 320 --weights '/content/cup-disc-Segmentation/weights/weight.pt' --source '/path to/fundus.jpg' --name custom-dataset
```
6. 
