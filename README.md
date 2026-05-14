# IMPLEMENTATION-OF-OPENING-AND-CLOSING
## Aim :
To implement Opening and Closing using Python and OpenCV. 

## Software Required Anaconda -
```
Python 3.7 
OpenCV
```

## Algorithm: 

```
Step1: Import the necessary packages
Step2: Create the Text using cv2.putText
Step3: Create the structuring element
Step4: Use Opening operation
Step5: Use Closing Operation
```

## Name: Oviya N
## Reg.No:212223040140

## Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Oviya', (50, 250), cv2.FONT_HERSHEY_SIMPLEX, 3, (255, 255, 255), 5, cv2.LINE_AA)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```

## Output:

<img width="385" height="699" alt="image" src="https://github.com/user-attachments/assets/da926b8e-6cc4-4233-99d5-04a7bf498696" />

<img width="456" height="367" alt="image" src="https://github.com/user-attachments/assets/f0928245-6991-4c37-91c1-5a8a1cd4e5cd" />

<img width="460" height="360" alt="image" src="https://github.com/user-attachments/assets/35ff40d1-95ae-4f8e-9e4b-2bbb1a1703e6" />
<img width="458" height="369" alt="image" src="https://github.com/user-attachments/assets/1ad9943e-3723-4731-9358-74965d916e16" />

## Result:
Thus, the program for Opening and Closing using Python and OpenCV has executed successfully.
