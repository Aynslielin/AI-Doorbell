# AI-Doorbell
This is the AI-Doorbell Readme. In this page, it'll introduce our AI-Doorbell project of the MCU Interface and Driver Design course. Please enjoy!
- **Institution**-: National Taiwan Ocean University, Electrical Engineering Dept.
- **Instructor**-: Richard Kuo
- **Members**-: 林昕瑋(Hsin-Wei Lin), 吳玟頡, 邱筠婷, 陳微凌, 莊詠瑜, 溫翔宇

---
## **Introduction**
In this project, we would like to build an intellectual doorbell that alerts the user who the visitor is. Hence, we decided to integrate the face detection function, RTSP libraries, and Line Notify Application to send user the visitor's photo that alerts the user.

---

## **Main Functions**
## 1.Face Detection
This function would allow the camera to detect whether the object outside the door is human or not.
### Face Detection Image:
![](https://github.com/Aynslielin/AI-Doorbell/blob/main/face%20detection.jpg)

## 2.Capture Image (transfer photo to Google Drive)
This function would capture images when the doorbell detects the faces outside the door.

## 3.Google Appscipts & Line notify (ifttt sent the photo from Google Drive to Line notify)
This function will transfer the images that the doorbell captured and send the photo to the Google Drive. And we use the ifttt to connect Google Drive and Line notify, then ifttt will make Line notify send the photo that the Drive recieved to our Line and show the image. So we can see who is outside the door.

### Code of Google Appscript:
https://script.google.com/macros/s/AKfycbxADuxUreZnrB5_0JEkr9j_94QvyhGlU7xKOwo7H2MjJ0tIMixrALXS8bcJQ7dAqk-PeQ/exec

or

https://github.com/Aynslielin/AI-Doorbell/blob/main/Google%20Appscript%20Code

### Folder of Google Drive:
https://drive.google.com/drive/folders/1US1-obtD7ScF2JX0lzY9FZSsrJnKf9m0?usp=sharing

### Line Notify Image:
![](https://github.com/Aynslielin/AI-Doorbell/blob/main/line%20notify.jpg)

### **Videos of Operating**
video1:https://youtu.be/YFg1xQlTuxs](https://www.youtube.com/watch?v=YFg1xQlTuxs&t=0s)

video2:https://www.youtube.com/watch?v=IumI-uAtkRU&t=0s

---

## **Materials and Tools** 
### **Realtek AMB82-mini**
![](https://www.amebaiot.com/wp-content/uploads/2023/03/amb82_mini.png)
https://rkuo2000.github.io/EdgeAI-course/lecture/2024/03/01/Edge-AI-MCU-Intro.html
[RTL8735B](https://www.amebaiot.com/en/amebapro2/): 32-bit Arm v8M, up to 500MHz, 768KB ROM, 512KB RAM, 16MB Flash (MCM embedded DDR2/DDR3L up to 128MB)
802.11 a/b/g/n WiFi 2.4GHz/5GHz, BLE 5.1, NN Engine 0.4 TOPS, Crypto Engine, Audo Codec, …

[Ameba Arduino](https://www.amebaiot.com/en/ameba-arduino-summary/)

[Amebapro2 AMB82-mini Arduino Example Guides](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-peripherals-examples)

[Amebapro2 AMB82-mini Arduino getting started](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-getting-started/)

### **JXF37 1920x1080 CMOS Image Sensor**
![](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.oemcameramodules.com%2Fsale-40210774-jx-f37p-sensor-2mp-1080p-30fps-mipi-camera-module-high-performance.html&psig=AOvVaw3r8-VujZpHSSWCg1oCGWF_&ust=1763127993153000&source=images&cd=vfe&opi=89978449&ved=0CBUQjRxqFwoTCNipveGh75ADFQAAAAAdAAAAABAE)
