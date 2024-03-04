# awesome-text-deskew

A curated list of awesome projects for image text skew detection/correction.


Let’s categorize according to solutions:

- [OpenCV rectangle](#opencv-rectangle)
- [Hough Transform](#hough-transform)
- [EAST model](#east-model)
- [Projection score](#projection-score)
- [Radon transform](#radon-transform)
- [Fourier Transform](#fourier-transform)


## OpenCV rectangle

Get angle from minimum bounding rectangle of text contours.

1. Detect the contours in the image, which includes text
2. Obtain the minimum bounding rectangle based on the contours
3. Retrieve the angle of the bounding rectangle

- [Skew Correction for Text Python] - code @github
- [Text skew correction with OpenCV and Python] - article @pyimagesearch
- [Text Documents Skewness Correction using OpenCV] article @medium

[Skew Correction for Text Python]: https://github.com/JafirDon/Skew-Correction-for-Text-Python
[Text skew correction with OpenCV and Python]: https://pyimagesearch.com/2017/02/20/text-skew-correction-opencv-python/
[Text Documents Skewness Correction using OpenCV]: https://netraneupane.medium.com/text-skewness-correction-a51fd3a27157


## Hough Transform

Get angle from line by the hough transform.

1. Calculate Hough lines in the image
2. Find the angle of the majority of lines

- [How-to deskew an nimage] - article @codeproject
- [Text Document Alignment using Probabilistic Houghline Transform] - article @medium
- [Skew Detection and Correction of Document images using Hough Transform] - article @muthu
    - also jupyer [notebook](https://github.com/muthuspark/ml_research/blob/master/Skew%20angle%20detection%20and%20correction%20using%20Hough%20Transform.ipynb) on github
- [Correcting Image Rotation with Hough Transform] - article @medium
    - also jupyer [notebook](https://github.com/stephanefschwarz/Hough-Transform/blob/master/HoughTransform.ipynb) on github
- [deskew with Hough Transform] - gist @github
- [Alyn] - code @github

[How-to deskew an nimage]: https://www.codeproject.com/Articles/13615/
[Text Document Alignment using Probabilistic Houghline Transform]: https://netraneupane.medium.com/document-image-alignment-97b61eeffb20
[Skew Detection and Correction of Document images using Hough Transform]: https://www.muthu.co/skew-detection-and-correction-of-document-images-using-hough-transform/
[Correcting Image Rotation with Hough Transform]: https://medium.com/wearesinch/correcting-image-rotation-with-hough-transform-e902a22ad988
[deskew with Hough Transform]: https://gist.github.com/AdroitAnandAI/46a7fa78ca0e018bfa4c340836844131
[Alyn]: https://github.com/kakul/Alyn


## EAST model

Get angle from text regions detected by the EAST model.

1. Detect the position of text regions,
2. Retrieve the angle of the region bounding box,
3. Calculate the average tilt angle.

- [Building a Scalable Image Orientation Correction System] article @medium
    - also in project [Anuvaad](https://github.com/project-anuvaad/anuvaad/blob/c8c61cdc2b94c6a93578b7b652027d3c041b93cc/anuvaad-etl/anuvaad-extractor/document-processor/pre-processor/src/services/orientation_correction.py#L123)

[Building a Scalable Image Orientation Correction System]: https://medium.com/@srihari_m_n/building-a-scalable-image-orientation-correction-system-a7214d6d879c


## Projection score

Get angle with the minimum pixel density projection

same like [Radon transform](#radon-transform)
1. Rotate the image at multiple angles
2. Calculate the cumulative sum of pixel values along each row
3. Find the angle with the highest cumulative sum

- [Detect text orientation] - question @stackoverflow
- [Deskew document images] - code @github
- [Python OpenCV skew correction for OCR] - question @stackoverflow
- [Projection to correct image skew and identify text lines] - code @github

[Detect text orientation]: https://stackoverflow.com/questions/23783061/detect-text-orientation
[Deskew document images]: https://github.com/amulyakali/skew-correction
[Python OpenCV skew correction for OCR]: https://stackoverflow.com/questions/57964634/python-opencv-skew-correction-for-ocr
[Projection to correct image skew and identify text lines]: https://github.com/microsoft/knowledge-extraction-recipes-forms/tree/master/Pre_Processing/Projection


## Radon transform

Get angle with alternating pixel density projection

1. Rotate the image at multiple angles
2. Calculate the cumulative sum of pixel values along each row
3. Find the angle with the highest cumulative sum or alternating cumulative sums


[Detecting rotation and line spacing of image of page of text using Radon transform] - gist @github

["River" detection in text] - question @stackoverflow


[Detecting rotation and line spacing of image of page of text using Radon transform]: https://gist.github.com/endolith/334196bac1cac45a4893
["River" detection in text]: https://dsp.stackexchange.com/questions/374/river-detection-in-text/377#377


## Fourier Transform

- [Document Skewness Detection and Correction] - article @medium
    - also python [code](https://github.com/np-n/blog_code_snippets/tree/master/Document%20Skewness%20Detection%20and%20Correction) on github
- [Document Image Skew Estimation] - paper @github

[Document Skewness Detection and Correction]: https://netraneupane.medium.com/document-skewness-detection-and-correction-8ba8204b5577
[Document Image Skew Estimation]: https://github.com/phamquiluan/jdeskew
