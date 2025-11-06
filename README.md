# Quiz-2-Tec-284-Spencer



from gpiozero import LED, Button
import time

# buttons and led
red_button = Button(25)     
green_button = Button(18)
blue_button = Button(23)

red_led = LED(17)
green_led = LED(27)
blue_led = LED(22)

print("Program start")

# main loop
def main():
    # Red LED
    #print("hello")
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
    
    time.sleep(0.2)  

while True:
    main()
    
if __name__ == "__main__":
    main()



