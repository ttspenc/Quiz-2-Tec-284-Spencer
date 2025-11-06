# Quiz-2-Tec-284-Spencer

from gpiozero import LED, Button
import time

# 
red_button = Button(7)     # change pins as needed
green_button = Button(8)
blue_button = Button(9)

red_led = LED(17)
green_led = LED(27)
blue_led = LED(22)

print("Program started. Press a button to turn on its color LED.")

# main loop
while True:
    # Red LED logic
    if red_button.is_pressed:
        red_led.on()
        print("Red button pressed, red on")
    else:
        red_led.off()
    
    # Green LED
    if green_button.is_pressed:
        green_led.on()
        print("Green button pressed, green on")
    else:
        green_led.off()
    
    # Blue LED
    if blue_button.is_pressed:
        blue_led.on()
        print("Blue button pressed, blue on")
    else:
        blue_led.off()
    
    time.sleep(0.2)  # keeps print messages readable

