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

Sivann的SmartPower模組可偵測電流值以及控制Relay的NC/NO，模組上有ACS712ELCTR-05B-T感測器以及TRB1-05D繼電器。  
ACS712ELCTR-05B-T可感測電流值，其相關的詳細資料在Reference，請自行參閱。  
#### Sivann模組疊合  
Sivann除了感測模組外還有供電模組及無線模組，使用者可以將模組疊合使用，更為方便，相關介紹在sivann模組疊合介紹。  
#### Features  
 * 量測AC/DC電流，電流值最大不超過3A  
 * 控制繼電器NC/NO  

<a name="Hardware Overview"></a>
## 2. Hardware Overview  

![Smart Power Relay](http://i.imgur.com/GWADze7.png "Smart Power Relay")  

#### Pinouts  
* Power Pins:  
  * 5V – 供電給繼電器及ACS712使用。  
  * Vcc(3.3V) – 供電給光耦合器。  
  * GND – 5V及Vcc共同的地。   
* AO  
ACS712的電壓輸出。  
* DIN  
控制繼電器NC/NO。  
* 5VCal  
給設計者一參考電壓，數值為5V的一半。主要是為了設計者在設計電流轉換時所需要的電壓基準值(詳細請參考Reference的ACS712)。  
* PIR(optional)  
讀取PIR狀態。  

<a name="Usage"></a>
## 3. Usage  

供電5V及Vcc並接好GND。  
將待量測電流事物接於COM及NC/NO。  

<a name="Reference"></a>
## 4. Reference  
 
[ACS712 Datasheets](http://pdf1.alldatasheet.com/datasheet-pdf/view/168326/ALLEGRO/ACS712.html "ACS712")  
Schematic  

