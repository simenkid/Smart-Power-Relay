[TODO]  
1. 模組疊合  
2.   

# Smart Power Relay  
---  

## Guide Content  

1. [Introduction](#Introduction)  
2. [Hardware Overview](#Hardware Overview)  
3. [Usage](#Usage)  
4. [Reference](#Reference)  


<a name="Introduction"></a>
## 1. Introduction  

Sivann 的 SmartPowerRelay 模組有繼電器當開關以及電流感測器，這可以切關電器開關和量測電流值。電流感測器 (ACS712ELCTR-05B-T) 以及繼電器 (TRB1-05D) ，其相關的詳細資料在 Reference ，請自行參閱。  

#### Sivann模組疊合  
Sivann 有感測模組外、無線模組以及電源模組，使用者可以將模組疊合使用，相關介紹在 sivann 模組疊合介紹。  
#### Features  
 * 量測AC/DC電流，電流值最大不超過3A。  
 * 控制繼電器NC/NO。  

<a name="Hardware Overview"></a>
## 2. Hardware Overview  

![Smart Power Relay](http://i.imgur.com/GWADze7m.png "Smart Power Relay")  

#### Pinouts  
* Power Pins:  
  * 5V – 5V 的電源腳位。供電給繼電器及ACS712使用。  
  * Vcc (3.3V) – 3.3V 的電源腳位。供電給光耦合器。  
  * GND – 5V及Vcc共同的地。   
* AO  
ACS712的電流資訊 (電壓型態)。  
* DIN  
控制繼電器 NO/NC ，繼電器的 NO/NC 對應於 DIN 的電壓0V/3.3V。  
* 5VCal  
參考電壓，數值為5V的一半。主要是為了設計者在設計電流轉換時所需要的電壓基準值(詳情請參考Reference的ACS712)。  
* PIR(optional)  
讀取 PIR 狀態。對於設計者，這是選擇性的腳位，可以藉由 PIR 腳位來設計用其他方式來控制繼電器的狀態。  

<a name="Usage"></a>
## 3. Usage  

1.	連接 5V 及Vcc (3.3V) 至電源供應。
2.	連接 GND 至電源供應的地。
3.	連接 DIN 至微控制器的輸出腳位或是供電0/3.3V。
4.	連接 AO 和 5VCal 至微控制器的 ADC 輸入腳位。  
5.	連接電器，如下圖所示。

<a name="Reference"></a>
## 4. Reference  
 
[ACS712 Datasheets](http://pdf1.alldatasheet.com/datasheet-pdf/view/168326/ALLEGRO/ACS712.html "ACS712")  
Schematic  

