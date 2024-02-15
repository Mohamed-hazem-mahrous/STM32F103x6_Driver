# STM32F103x6 Driver

This repository contains drivers for the STM32F103x6 microcontroller.

## Table of Contents

- [Overview](#overview)
- [Folder Structure](#folder-structure)
- [Usage](#usage)
- [Contributing](#contributing)
- [Author](#author)

## Overview

The STM32F103x6 Driver is a collection of drivers for various peripherals of the STM32F103x6 microcontroller. It includes drivers for GPIO, EXTI, RCC, USART, keypad, LCD and Servo Motor peripherals.

## Folder Structure

The project structure is organized as follows:
### MCAl
#### Includes
- STM32F103x8.h
- stm32f103x8_EXTI_driver.h
- stm32f103x8_gpio_driver.h
- stm32f103x8_RCC_driver.h
- stm32f103x8_USART_driver.h
- stm32f103x8_SPI_driver.h
#### Implementation
- stm32f103x8_EXTI_driver.c
- stm32f103x8_gpio_driver.c
- stm32f103x8_RCC_driver.c
- stm32f103x8_USART_driver.c
- stm32f103x8_SPI_driver.c


### HAL
#### KEYPAD_DRIVER
- keypad.c
- keypad.h
#### LCD_DRIVER
- lcd.c
- lcd.h
#### Servo Motor
- servo.c
- servo.h

### Info

- `stm32f103x8_EXTI_driver.c` and `stm32f103x8_gpio_driver.c` contain the implementation of the EXTI and GPIO drivers.
- `stm32f103x8_RCC_driver.h` contain the implementation of the RCC driver.
- `stm32f103x8_USART_driver.h` contain the implementation of the USART driver.
- `stm32f103x8_SPI_driver.h` contain the implementation of the SPI driver.
- The `inc` folder includes header files for the drivers and `STM32F103x8.h` which defines base addresses and registers for the STM32F103x6 microcontroller.
- The `KEYPAD_DRIVER` folder contains the keypad driver implementation.
- The `LCD_DRIVER` folder contains the LCD driver implementation.
- The `Servo Motor` folder contains the Servo Motor driver implementation.


## Usage

You can use these drivers to interface with the STM32F103x6 microcontroller peripherals.
Make sure to configure your development environment and toolchain to compile and flash this code onto your STM32F103x6/x8 microcontroller.

## Contributing
Contributions to this project are welcome! If you find a bug or have an enhancement in mind, please open an issue or submit a pull request.

## Author
Mohamed Hazem Yahya Mahrous Ali - Biomedical and Embedded Engineering Student