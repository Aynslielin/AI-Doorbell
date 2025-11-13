# AI-Doorbell
This is the AI-Doorbell Readme. In this page, it'll introduce our AI-Doorbell project of the MCU Interface and Driver Design course. Please enjoy!
-**Institution**-: National Taiwan Ocean University, Electrical Engineering Dept.
-**Instructor**-: Richard Kuo
-**Members**-: 林昕瑋(Hsin-Wei Lin), 吳玟頡, 邱筠婷, 陳微凌, 莊詠瑜, 溫翔宇

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

## **Materials** 
### **Realtek AMB82-mini**
![](https://www.amebaiot.com/wp-content/uploads/2023/03/amb82_mini.png)
https://rkuo2000.github.io/EdgeAI-course/lecture/2024/03/01/Edge-AI-MCU-Intro.html
[RTL8735B](https://www.amebaiot.com/en/amebapro2/): 32-bit Arm v8M, up to 500MHz, 768KB ROM, 512KB RAM, 16MB Flash (MCM embedded DDR2/DDR3L up to 128MB)
802.11 a/b/g/n WiFi 2.4GHz/5GHz, BLE 5.1, NN Engine 0.4 TOPS, Crypto Engine, Audo Codec, …

[Ameba Arduino](https://www.amebaiot.com/en/ameba-arduino-summary/)

[Amebapro2 AMB82-mini Arduino Example Guides](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-peripherals-examples)

[Amebapro2 AMB82-mini Arduino getting started](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-getting-started/)

***

## **MCU Interfaces introduction**

### **GPIO (General Purpose I/O)**

![](https://github.com/rkuo2000/MCU-course/blob/main/images/GPIO_circuit_diagram.png?raw=true)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/GPIO_LED_circuit.png?raw=true)

***
### **ADC (Analog Digital Converter)**

![](https://rockuapps.com/wp-content/uploads/2020/11/c-1-791x613.jpg)

**Vin**is input voltage for ADC to sample

**Vref** is reference voltage for ADC to compare with Vin

**2-bit ADC**


![comb74](https://github.com/Aynslielin/portable-chatgpt/assets/161717296/f520773a-ec36-4ee0-8bea-f212facaf8dd)
![](https://qph.fs.quoracdn.net/main-qimg-fa7473dd759a220592359c69ca8408a2)

***


**12-bit ADC** output is a 12-bit binary code, so its value = 0 ~ 4095
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ADC_12bit_table.png?raw=true)

### **Direct-Conversion ADC**

![](https://www.maximintegrated.com/content/dam/images/design/tech-docs/634/E33Fig01.gif)

### **Successive-Approximation ADC**

![](https://github.com/rkuo2000/MCU-course/blob/main/images/SA_ADC_block_diagram.png?raw=true)

### **Sigma-Delta ADC**

![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sigma-Delta_ADC_block_diagram.png?raw=true)

***
### **DAC (Digital to Analog Converter)**

[Introduction to Digital-Analog Conversion](https://www.allaboutcircuits.com/textbook/digital/chpt-13/digital-analog-conversion/)
### **Binary-Weighted Resistor DAC**

![](https://www.allaboutcircuits.com/uploads/articles/inverting-summing-circuit-diagram.jpg)
![](https://www.allaboutcircuits.com/uploads/articles/6-bit-binary-weighted-DAC.jpg)

***
### **PWM (Pulse Width Modulation)**

![](https://github.com/rkuo2000/MCU-course/blob/main/images/PWM_functional_diagram.png?raw=true)
CMR >= CNR: PWM output high
CMR < CNR: PWM output low
**PWM Frequency**= PWM_Clock/(prescale)*(clock divider)/ CNR
**Duty ratio**= CMR /CNR
![](https://microcontrollerslab.com/wp-content/uploads/2019/04/Servo-motor-pinout-esp32.png)

***
### **I2C (Inter-Integrated Circuit bus)**

[I2C bus 簡介](https://magicjackting.pixnet.net/blog/post/173061691-i2c-bus-%E7%B0%A1%E4%BB%8B-(inter-integrated-circuit-bus)-)
![](https://pic.pimg.tw/magicjackting/1447382351-2909185260.png)
![](https://pic.pimg.tw/magicjackting/1447739085-239160220.png)
![](https://pic.pimg.tw/magicjackting/1450787341-3597609114_n.png?v=1461809344)
![](https://pic.pimg.tw/magicjackting/1461659401-258467416.png)
![](https://github.com/rkuo2000/EdgeAI-course/blob/main/images/Example_BMP085.jpg?raw=true)
![](https://github.com/rkuo2000/EdgeAI-course/blob/main/images/Example_BMP280.jpg?raw=true)

***
### **SPI (Serial peripheral interface)**

[Introduction to SPI Interface](https://www.analog.com/en/analog-dialogue/articles/introduction-to-spi-interface.html)
4-wire SPI devices have four signals:
* **CS** : Chip select
* **SCLK**: SPI Clock
* **MOSI**: Master out, slave in
* **MISO**: Master in, slave out
![](https://www.analog.com/-/media/images/analog-dialogue/en/volume-52/number-3/articles/introduction-to-spi-interface/205973_fig_01.png?la=en&imgver=2)

***
### **I2S (Inter-IC Sound bus)**

[Introduction to the I2S Interface](https://www.allaboutcircuits.com/technical-articles/introduction-to-the-i2s-interface/)
![](https://www.allaboutcircuits.com/uploads/articles/introduction-to-the-i2s-interface_rk_aac_image1.jpg)
![](https://www.allaboutcircuits.com/uploads/articles/introduction-to-the-i2s-interface_rk_aac_image2.jpg)

***
### **UART（Universal Asynchronous Receiver/Transmitter）序列埠**

[BASICS OF UART COMMUNICATION](https://www.circuitbasics.com/basics-uart-communication/)
![](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-UART-Data-Transmission-Diagram.png)
![](https://makerpro.cc/wp-content/uploads/2019/08/2.png)
Protocol 通訊協定
![](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-UART-Packet-Frame-and-Bits-2.png)
* Standard Packet : 8 data bits, even parity, 1 stop bit
1. If the parity bit is a 0 (even parity), the 1 bits in the data frame should total to an even number.
2. If the parity bit is a 1 (odd parity), the 1 bits in the data frame should total to an odd number.
![](https://makerpro.cc/wp-content/uploads/2019/08/4.png)
RS232 的Vpp電壓較高，有 6V~30V；UART 則是較低的 3.3V 或 5V
RS232 為負邏輯， UART 為正邏輯，因此兩者波形是反相的**Baud Rate**

_This site was last updated March 16, 2024._


