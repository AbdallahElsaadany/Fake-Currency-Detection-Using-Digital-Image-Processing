# Fake-Currency-Detection-Using-Digital-Image-Processing

## Introduction
Fake currency is a significant issue faced by financial institutions and individuals worldwide. Counterfeit money can have severe economic consequences, leading to financial losses and undermining the trust in the monetary system. To combat this problem, digital image processing techniques can be employed to detect fake currency notes.

This project aims to develop a system that leverages digital image processing algorithms to detect counterfeit currency. By analyzing various features and patterns on currency notes, the system can identify potential discrepancies that indicate the presence of fake currency.

## Methodology
### Method 1: UltraViolet effect
The first method in the fake currency detection process is simulating the **ultraviolet effect** on the fake image. 
This method is based on this [Paper](https://www.researchgate.net/publication/365977982_COUNTERFEIT_CURRENCY_DETECTION_USING_IMAGE_PROCESSING).
The following steps are followed in this method:

1. Convert the Image to HSV Color Space
2. Apply Histogram Equalization on The Image
3. Compare the mean saturation of the current Image with the reference image


### Method 2: Feature Extraction
The first method in the fake currency detection process is **extracting features** from the Current image and comparing them with the extracted features of the reference Image.
The features that we have focused on are **(Blendlines, Serial number & Font size).**
The following steps are followed in this method:

1. Convert the Image to gray Color Space
2. use the canny detector to detect edges
3. Apply Closing to connect objects to each other
4. Apply Region filling
5. Apply Edge-based segmentation

### Results

![alt text](data:image/jpeg;base64,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)


### References
- https://www.researchgate.net/publication/365977982_COUNTERFEIT_CURRENCY_DETECTION_USING_IMAGE_PROCESSING
- https://iopscience.iop.org/article/10.1088/1757-899X/263/5/052047
- https://ijcsmc.com/docs/papers/April2019/V8I4201914.pdf
- https://www.mintageworld.com/knowledge-base/security-features-on-current-banknotes/







This method is based on this [Paper](https://www.researchgate.net/publication/365977982_COUNTERFEIT_CURRENCY_DETECTION_USING_IMAGE_PROCESSING).

https://iopscience.iop.org/article/10.1088/1757-899X/263/5/052047
