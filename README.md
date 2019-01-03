# Nucleo-H743ZI + Ethernet + LwIP (without RTOS) + HTTPD
About:
* Working (tested) example of **LwIP** stack usage (without RTOS) with web server functionality.
* This example uses static IP address **192.168.1.100** (/24) and port **80** for the web server.

How to test it?
* Power up the **Nucleo-H743ZI** board (connect to USB port or use external 5V/3.3V)
* Connect **Nucleo-H743ZI** board to your PC (or router) using **Ethernet** cable
* Setup **IP / network mask** for the PC as **192.168.1.XXX / 255.255.255.0** (XXX = 1-99 or 99-254)
* Use your favorite browser and open the URL - http://192.168.1.100/
