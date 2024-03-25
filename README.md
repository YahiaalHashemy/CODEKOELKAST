from gpiozero import LED, Buzzer 

from time import sleep 

import os 

import time  

from gpiozero import Button 

  

red = LED (18) 

blue = LED (24) 

buzzer = Buzzer (22) 

  

while True:  

  print("lights and sound on") 

  red.on() 

  blue.on() 

  buzzer.on() 

  sleep(0.2) 

  

  print("lights and sound off") 

  red.off() 

  blue.off() 

  buzzer.off() 

  sleep(0.2) 

   

button = Button(15) 

print("_____________") 

print("Button + GPIO") 

print("_____________") 

  

while True: 

    if (button.is_pressed): 

        print("Button pressed") 

        time.sleep(1) 

    else: 

        os.system("clear") 

        print("Waiting for you to press the button") 

         

    time.sleep(0.5) 

import time 

from w1thermsensor import W1ThermSensor 

  

sensor = W1ThermSensor() 

  

while True: 

    temperature = sensor.get_temperature() 

    print("de temperatuur is %s graden Celsius" % temperature) 

     

    time.sleep(1) 
