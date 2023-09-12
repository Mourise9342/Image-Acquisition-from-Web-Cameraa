# Image-Acquisition-from-Web-Cameraa
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

## Program:

### Developed By:Mourise jane
### Register No:212222230085

## i) Write the frame as JPG file
     ```
     import cv2
     img = cv2.VideoCapture(0)
     while(True):
          imagee,frame = img.read()
          cv2.imshow('myimage',frame)
          if cv2.waitKey(1) == ord('c'):
               breakc
     img.release()
     cv2.destroyAllWindows()
     ```



## ii) Display the video
```
import cv2
video = cv2.VideoCapture(0)
while (True):
    cap,frame=video.read()
    cv2.imshow('Capturing Video',frame)
    if cv2.waitKey(1) == ord('q'):
        break
video.release()


```




## iii) Display the video by resizing the window

```
import cv2
import numpy as np
img  = cv2.VideoCapture(0)
while True:
    pic,frame = img.read()
    width = int(img.get(3))
    height = int(img.get(4))
    image = np.zeros(frame.shape, np.uint8)
    small_frame = cv2.resize(frame,(0,0),fx =0.5, fy = 0.5)
    image[:height//2, :width//2]=small_frame
    image[height//2:, :width//2]=small_frame
    image[:height//2, width//2:]=small_frame
    image[height//2:, width//2:]=small_frame
    cv2.imshow('myimage',image)
    if cv2.waitKey(1) == ord('c'):
        break
img.release()
cv2.destroyAllWindows()

```



## iv) Rotate and display the video

```

import cv2
import numpy as np
img  = cv2.VideoCapture(0)
while True:
    pic,frame = img.read()
    width = int(img.get(3))
    height = int(img.get(4))
    image = np.zeros(frame.shape, np.uint8)
    small_frame = cv2.resize(frame,(0,0),fx =0.5, fy = 0.5)
    image[:height//2, :width//2]=cv2.rotate(small_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=small_frame
    image[:height//2, width//2:]=small_frame
    image[height//2:, width//2:]=cv2.rotate(small_frame,cv2.ROTATE_180)
    cv2.imshow('myimage',image)
    if cv2.waitKey(1) == ord('c'):
        break
img.release()
cv2.destroyAllWindows()








```
## Output

### i) Write the frame as JPG image

![t jpg](https://github.com/Jayakrishnan22003251/Image-Acquisition-from-Web-Cameraa/assets/120232371/d96d560b-ac4e-4a36-b52b-742205052363)


### ii) Display the video
![Screenshot (109)](https://github.com/Jayakrishnan22003251/Image-Acquisition-from-Web-Cameraa/assets/120232371/68c012b5-a790-4f78-bcd1-6d970dfb4395)



### iii) Display the video by resizing the window





### iv) Rotate and display the video
![Uploading image.png…]()





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
