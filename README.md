# Basic-Image-Manipulation
## Aim:
To do the basic image manipulation on a image
## Procedure:
## Code:
## Exercise 1
```
import cv2
from matplotlib import pyplot as plt
image = cv2.imread('apollo.jpg', cv2.IMREAD_GRAYSCALE)
height, width = image.shape
print("Width:", width)
print("Height:", height)
plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off') 
plt.show()
cv2.imwrite('apollo.png', image)
image = cv2.imread('apollo.jpg')
rect_color = (255, 0, 255)
text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
font_thickness = 2
text_color = (0, 255, 0) 
text_size, _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_size[0]) // 2
text_y = image.shape[0] - 50  
cv2.putText(image, text, (text_x, text_y), font_face, font_scale, text_color, font_thickness)
rect_color = (255, 0, 255)  
top_left = (500, 100)  
bottom_right = (700, 600) 
cv2.rectangle(image, top_left, bottom_right, rect_color, 5)
plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```
## Exercise 2
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('natDIP.jpg', cv2.IMREAD_COLOR)
print("Original image shape:", img.shape)
gray_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
print("Grayscale image shape:", gray_img.shape)
plt.figure(figsize=(10, 10))
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis('off')
plt.imshow(gray_img, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
plt.show()
x, y, w, h = 250, 100, 300, 200
cropped_img = img[y:y+h, x:x+w]
resized_img = cv2.resize(cropped_img, None, fx=2, fy=2)
flipped_img = cv2.flip(resized_img, 1)
plt.figure(figsize=(5, 5))
plt.imshow(flipped_img[:, :, ::-1])   
plt.yticks([0, 50, 100, 150, 200, 250, 300, 350])  
plt.xticks([0, 50, 100, 150, 200, 250, 300, 350])  
plt.show()
```
## Output:
## Exercise 01

![image](https://github.com/user-attachments/assets/0d72593f-43ba-4873-8965-d18369f7036b)


![image](https://github.com/user-attachments/assets/16277340-cbf3-446f-b2a3-16d2e4a8d68e)


## Exercise 02

![image](https://github.com/user-attachments/assets/b68e3c62-87a2-451c-9c07-585f3ca7e8cc)

![image](https://github.com/user-attachments/assets/fe94d534-b146-4c76-a151-aaa82223b997)

![image](https://github.com/user-attachments/assets/aaad8a6d-b70c-46d0-b90f-f38434fae69c)



## Result:
Thus, the program has been successfully executed

