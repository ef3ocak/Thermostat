STM32
This project implements a PWM-based temperature-controlled fan system using an STM32 microcontroller.


Description

The system reads temperature data from an analog sensor via ADC, displays the temperature on an SSD1306 OLED screen, and controls a DC fan using PWM (TIM3) according to predefined temperature thresholds. Visual (LED) and audible (buzzer) indicators are used for status and warnings.


Features

* ADC-based temperature measurement
* PWM fan speed control (0%, 50%, 100%)
* OLED display (SSD1306, I²C)
* LED status indicators
* Buzzer alarm for high temperature
* UART output for debugging

Control Logic

* Temperature ≤ 35°C → Fan OFF (0%), LED1 ON
* Temperature 35–60°C → Fan 50% PWM, LED2 ON, short beep
* Temperature ≥ 60°C → Fan 100% PWM, LED3 ON, long beep
