# STM32F103x6 Driver

This repository contains drivers for the STM32F103x6 microcontroller.

## Table of Contents

- [Overview](#overview)
- [Folder Structure](#folder-structure)
- [Usage](#usage)
- [Contributing](#contributing)
- [Author](#author)

## Overview

The STM32F103x6 Driver is a collection of drivers for various peripherals of the STM32F103x6 microcontroller. It includes drivers for GPIO, EXTI, keypad, and LCD peripherals.

## Folder Structure

The project structure is organized as follows:

├── Stm32_F103C6_EXTI_driver.c
├── Stm32_F103C6_GPIO_driver.c
├── inc
│ ├── Stm32_F103C6_EXTI_driver.h
│ ├── Stm32_F103C6_gpio_driver.h
│ └── stm32f103x6.h
├── KEYPAD_DRIVER
│ ├── keypad.c
│ └── keypad.h
├──  LCD_DRIVER
│ ├── lcd.c
│ └── lcd.h
└──


- `Stm32_F103C6_EXTI_driver.c` and `Stm32_F103C6_GPIO_driver.c` contain the implementation of the EXTI and GPIO drivers.
- The `inc` folder includes header files for the drivers and `stm32f103x6.h`, which defines base addresses and registers for the STM32F103x6 microcontroller.
- The `KEYPAD_DRIVER` folder contains the keypad driver implementation.
- The `LCD_DRIVER` folder contains the LCD driver implementation.

## Usage

You can use these drivers to interface with the STM32F103x6 microcontroller peripherals. Here's a basic example of how to use the GPIO driver to toggle an LED:

```c
#include "Stm32_F103C6_GPIO_driver.h"

int main(void) {
    // Initialize GPIO for an LED connected to pin GPIO_PIN_13
    GPIO_Handle_t gpioLed;
    gpioLed.pGPIOx = GPIOA; // Change to the appropriate GPIO port
    gpioLed.GPIO_PinConfig.GPIO_PinNumber = GPIO_PIN_13;
    gpioLed.GPIO_PinConfig.GPIO_PinMode = GPIO_MODE_OUT_PP;
    gpioLed.GPIO_PinConfig.GPIO_PinSpeed = GPIO_SPEED_HIGH;

    GPIO_Init(&gpioLed);

    while (1) {
        // Toggle the LED
        GPIO_TogglePin(GPIOA, GPIO_PIN_13);

        // Delay for some time
        for (int i = 0; i < 100000; i++);
    }

    return 0;
}
```

Make sure to configure your development environment and toolchain to compile and flash this code onto your STM32F103x6 microcontroller.

## Contributing
Contributions to this project are welcome! If you find a bug or have an enhancement in mind, please open an issue or submit a pull request.

## Author
Mohamed Hazem Yahya Mahrous Ali - Biomedical and Embedded Engineering Student