# wnb
Objective-

You can see the notice boards being used specially at offices and public places to display important news and notices. 
To make the notice boards easy to use and more technically advance, I have used this prototype of wireless notice board where we can display the message by simply sending the message through your cell phone.
These display systems are very accurate and easy to control and cheaply available and the most important thing is that they can be operated on low Voltage (Up to 12 Voltage).
A GSM module is used here for the wireless notice board to send the information or message to display. The main aim of this project is to save time and provide information urgently on display for the customers.
In this circuit GSM module and a 16×2 LCD display is used for receiving message and display message respectively. When any urgent information is to share with more people this system works perfectly. When anyone wants to show any information or message, then sender sends a SMS to GSM Module. Then Arduino reads the GSM module and send it to the LCD. This project can be improved by using a larger display module. Here are few links to the images showing the working of this project.


https://engineersgarag.wpengine.com/wp-content/uploads/2019/07/Prototype-Arduino-Based-Wireless-Notice-Board-Schools.jpg
https://engineersgarag.wpengine.com/wp-content/uploads/2019/07/Image-Arduino-Based-Wireless-Notice-Board-Designed-Schools.jpg
https://engineersgarag.wpengine.com/wp-content/uploads/2019/07/Image-Sms-Used-Send-Notice-Wireless-Notice-Board.jpg
https://engineersgarag.wpengine.com/wp-content/uploads/2019/07/Image-Display-Panel-Wireless-Notice-Board.jpg

Technical Details-

This circuit is build by using GSM and 16X2 liquid crystal display and both these are controlled by using arduino mini pro. In this circuit, liquid crystal display is connected in 4 bit mode means only four data pins of liquid crystal display are used. And rw pin of liquid crystal display directly connected to the ground. RS pin and EN pin is directly connected to digital pin 12 and digital pin 11 of arduino respectably. And Rx pin and Tx pin of GSM module is directly connected to Tx pin and Rx pin of arduino. There is no need of additional RS232 chip. Because GSM module already have a inbuild RS232 ic. All these connections are connected by using jumper wires.

Link to Block Diagram for the Project-

https://engineersgarag.wpengine.com/wp-content/uploads/2019/07/Block-Diagram-Arduino-Based-Wireless-Notice-Board.jpg


Programming part of this system is also very simple, GSM module in configured in direct message receiving mode using by applied AT command to GSM module that is:

AT+CMNI=2,2,0,0,0

After this configuration there is no need to send any other AT command to GSM module to read message from GSM module message storage. Here we read only serial data that is coming from GSM module serially.

Before reading message from GSM module we must enclosed the sending message between the * and #.

After receiving this encoded message from GSM module first stored this message in a temporarily defined array or string and then decoded this message by using suitable method or logic. Here I have used if statement for decoding the message. But here, you can use any logic to decode this message and you can also send your message without * and #.

 

Components used:

1.     Arduino Pro Mini

2.     GSM Module

3.     16X2 Liquid Crystal Display


Link to The Circuit Diagram-

https://www.engineersgarage.com/wp-content/uploads/2019/07/Circuit-Diagram-Arduino-Gsm-Gprs-Module-Based-Wireless-Notice-Board-Schools.png


REFERENCE-

https://youtu.be/88W4OkWU09k
