from pyA20.gpio import gpio
from pyA20.gpio import port
import time

# Set up GPIO
gpio.init()
# Define the GPIO pin number (using the port.PA2 for example)
LED_PIN = port.PA2
# Set the pin direction to output
gpio.setcfg(LED_PIN, gpio.OUTPUT)

try:
    while True:
        # Turn on the LED
        gpio.output(LED_PIN, gpio.HIGH)
        # Wait for 0.5 seconds
        time.sleep(0.5)
        # Turn off the LED
        gpio.output(LED_PIN, gpio.LOW)
        # Wait for 0.5 seconds
        time.sleep(0.5)

except KeyboardInterrupt:
    # If Ctrl+C is pressed, clean up GPIO
    gpio.output(LED_PIN, gpio.LOW)
