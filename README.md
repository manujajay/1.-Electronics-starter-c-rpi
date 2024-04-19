# Electronics Starter with Raspberry Pi

This repository is designed for beginners to explore basic electronics projects using the Raspberry Pi. It provides tutorials and examples to get started with simple circuits and interfacing various components.

## Prerequisites

- Raspberry Pi (any model that has GPIO pins)
- Basic electronic components (LEDs, resistors, sensors)
- Python 3 installed on Raspberry Pi

## Installation

Set up your Raspberry Pi with the latest version of Raspberry Pi OS. Make sure Python 3 and GPIO library are installed:

```bash
sudo apt update
sudo apt install python3 python3-gpiozero
```

## Example - Blinking LED

This example demonstrates how to control an LED via Raspberry Pi GPIO pins.

### `blinking_led.py`

```python
from gpiozero import LED
from time import sleep

# Setup the LED on GPIO pin 17
led = LED(17)

# Blinking loop
try:
    while True:
        led.on()
        print("LED on")
        sleep(1)
        led.off()
        print("LED off")
        sleep(1)
except KeyboardInterrupt:
    print("Program stopped by user.")
    led.off()
```

## Contributing

If you are interested in contributing to this project by adding more examples or improving documentation, please fork this repository, create a new branch for your edits, and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
