Assessing thermal imagery integration into object detection methods on air-based collection platforms
===================================================

Object detection models commonly focus on utilizing the visible spectrum via Red–Green–Blue (RGB) imagery. 

Due to various limitations with this approach in low visibility settings, there is growing interest in fusing RGB with thermal Long Wave Infrared (LWIR) (7.5–13.5 µm) images to increase object detection performance. 

However, we still lack baseline performance metrics evaluating RGB, LWIR and RGB-LWIR fused object detection machine learning models, especially from air-based platforms. 

This repository provides the code materials for a paper which undertakes such an evaluation, finding that a blended RGB-LWIR model generally exhibits superior performance compared to independent RGB or LWIR approaches. 

Citation
---------

- Gallagher, J.E. and Oughton, E.J. (2023) ‘Assessing thermal imagery integration into object detection methods on air-based collection platforms’, Scientific Reports, 13(1), p. 8491. Available at: https://doi.org/10.1038/s41598-023-34791-8.

Results
-------

An RGB-LWIR blend only performs 1–5% behind the RGB approach in predictive power across various altitudes and periods of clear visibility. Yet, RGB fusion with a thermal signature overlay provides edge redundancy and edge emphasis, both which are vital in supporting edge detection machine learning algorithms (especially in low visibility environments). 

This approach has the ability to improve object detection performance for a range of use cases in industrial, consumer, government, and military applications. This research greatly contributes to the study of multispectral object detection by quantifying key factors affecting model performance from drone platforms (including distance, time-of-day and sensor type). 

Repository Contents
-------------------

The first notebook (`RGB-LWIR_image_processor.ipynb`) is used to generate additional edge-defined images from an original image dataset. The notebook is currently set to generate six image processed images. 

The second notebook (`YOLOv7_train_test.ipynb`) is used to train and test YOLOv7 object detection models. Use the test_yaml and test.py files when testing images and labels to generate mAP. Upload the `test_yaml` to the data folder within the YOLOv7 folder. Add the `test.py` script into the main YOLOv7 folder. 

