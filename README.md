# Iris_mapping

To use this app, install the requirements and run the command ```python app.py```

It should be running on ```http://127.0.0.1:5000```. The initial page is shown in the figure below.

<p align="center">
<img src="https://github.com/user-attachments/assets/43cb7363-dd1a-4c3c-9ee6-dd7179e64fad" height="300" />
</p>

## 1. What this app does

This app is capable of finding and map the human iris, finding the contour of a face, isolate and crop a face and its eyes. 

## 2. How to use it

To use the app, just upload an image of a face, preferable frontal and with visible irises, as it shown on the example of the app. After that, just choose a task. The result can take a long time depending on the size of the image used. 

## 3. Expected results

Each option will return the resulting images in a new window. The figures below shows an example of iris color mapping, Facial Contour, Face Cut and  Eye Cut tasks, in that order.

<p align="center">
<img src="https://github.com/user-attachments/assets/ea78e491-17f3-41c2-b1ac-32d9bdf9b3e5" height="250" />
<img src="https://github.com/user-attachments/assets/c2cde3bb-0977-4e5d-9d68-71761ffefa89" height="250" />
<img src="https://github.com/user-attachments/assets/ca902940-e60c-4a58-971f-55453a76f51a" height="250" />
<img src="https://github.com/user-attachments/assets/a4cd24c6-c84f-4517-8d0b-d4419ad43f70" height="250" />
</p>

Many things can influence the results of the "Iris Color Mapping" task, suck as lighting, shadows, reflections, near closed eyes, among others. The module aims to give the exact color of each pixel of the bottom half of the iris, at the end computes the percentage of color found, which leads to interesting results of iris with many colors, as it is shown in the image below.

<p align="center">
<img src="https://github.com/user-attachments/assets/8bc32135-4731-493d-96a3-fef55ebd12e7" height="450" />
</p>

## 4. How it is done

The core of the app is a segmentation neural network created and trained by me. The result is post processed wit many others techniques such as K-means, color aproximations, conversions between colors spaces, among others. I choose to use only the bottom half of the iris due to the uooer half usualy been covered in a natural frontal position. 
