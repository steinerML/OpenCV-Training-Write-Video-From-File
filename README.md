# OpenCV Write Video from File.
Writing video from file using OpenCV.
## Contents :

In this the case I was writing from file using OpenCV.
I have used the following functions/methods:

| Function        |Action                                                                        | 
|----------------:|------------------------------------------------------------------------------|
|cv2.VideoCapture()   | Creates a video capture object, which would help stream or display the video.|
|**cv2.VideoWriter()**    | Saves the output video to a directory and takes 6 arguments.                 |
|     **filename**    |  Displays image.                                                             |
|    **apiPrefrence** |   API backends identifier                                                    |
|     **fourcc**      |  4-character code of codec, used to compress the frames                      |
|     **fps**         |  Frame rate of the created video stream                                      |
|     **frameSize**   |  Size of the video frames                                                    |
|     **isColor**     |  If not zero, the encoder will expect and encode color frames. Else it will work with grayscale frames.|


## Test Video used: 
I have used Cars.mp4 that can be found in the repository.

![Source Image Sequence](https://learnopencv.com/wp-content/uploads/2021/05/image.gif)


## Summary:

```python
#Creates capture object, reading video from webcam
vid_capture = cv2.VideoCapture('Cars.mp4')
```

```python
# Initialize video writer object
output = cv2.VideoWriter('output_from_file.mp4', cv2.VideoWriter_fourcc(*'DIVX'), 20, frame_size)

```
```python
# Different codec options for cv2.VideoWriter()
#AVI: cv2.VideoWriter_fourcc('M','J','P','G')
#MP4: cv2.VideoWriter_fourcc(*'XVID')
#DIVX MP4: cv2.VideoWriter_fourcc(*'DIVX')
#See table here: shorturl.at/dotBK

```
