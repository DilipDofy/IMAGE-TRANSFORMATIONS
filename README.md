# IMAGE-TRANSFORMATIONS
  
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules  

### Step2:
Choose an image and save it as filename.jpg

### Step3:
Use imread to read the image

### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:
Crop the image to remove unwanted areas from an image

### Step10:
Use cv2.imshow to show the image

### Step11:
End the program

## Program:
Developed By: DILIP M P
Register Number: 212223230048

i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Downloads\Gate way of india _Travel india.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Downloads\Gate way of india _Travel india.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()
```

iii)Image shearing
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Downloads\Gate way of india _Travel india.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```

iv)Image Reflection
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Downloads\Gate way of india _Travel india.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```

v)Image Rotation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Downloads\Gate way of india _Travel india.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Rotation:")
plt.imshow(translated_image)
plt.show()
```

vi)Image Cropping
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread(r"C:\Users\admin\Downloads\Gate way of india _Travel india.jpg")
h, w, _ = image.shape
cropped_face = image[int(h*0.2):int(h*0.8), int(w*0.3):int(w*0.7)]
cv2.imwrite("cropped_pigeon_face.jpg", cropped_face)
plt.imshow(cv2.cvtColor(cropped_face, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()
```

## Output:
### input image
![Screenshot 2025-04-29 091820](https://github.com/user-attachments/assets/bad5182a-2ee6-48e5-94f2-a984b666d0ec)



### i)Image Translation
![Screenshot 2025-04-29 091838](https://github.com/user-attachments/assets/4ad0fa34-d708-44a3-9207-feb888b13a03)




### ii) Image Scaling
![Screenshot 2025-04-29 091853](https://github.com/user-attachments/assets/af79da07-04ca-4fe5-bac8-2d8642271e60)





### iii)Image shearing
![Screenshot 2025-04-29 091911](https://github.com/user-attachments/assets/4ef7ba5a-b8b0-4030-b2f3-aa98dce03afe)






### iv)Image Reflection
![Screenshot 2025-04-29 091928](https://github.com/user-attachments/assets/a2e30b24-45af-4e6d-9fc9-04b1b04f8c86)




### v)Image Rotation
![Screenshot 2025-04-29 091943](https://github.com/user-attachments/assets/443bc62a-8786-4994-9c54-3901b317c308)




### vi)Image Cropping
![Screenshot 2025-04-29 091954](https://github.com/user-attachments/assets/1c8e6087-787b-4284-8be0-93814cf47be3)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
