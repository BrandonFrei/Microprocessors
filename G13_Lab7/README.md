The purpose of this lab was to learn to interact with the different sensors on the STM32L475 ARM-Cortex M4 board. The sensors used include: temperature, humidity, magnetometer, pressure, accelerometer, and gyroscope. 

One sensor was read at a time. Each press of the push button switched the current sensor, while holding the button down for 3 seconds turned off the UART and thread sensors.

This was implemented by using FreeRTOS. 3 threads were run concurrently while the chip was transmitting data: the UART thread, button press thread, and the sensor thread.

Each sensor was given its own thread, for a total of 6 sensor threads. Each time the button is pushed, the current sensor thread is shut down, and the next sensor thread is started in order to save power, as well as to free up processor space.
