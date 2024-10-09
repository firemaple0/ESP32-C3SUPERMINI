<h1><u><b># ESP32-C3SUPERMINI</b></u></h1>

Guide to use ESP32-C3 Supermini board that you Bought From Aliexpress
![Screenshot 2024-10-09 233340](https://github.com/user-attachments/assets/74b78114-7ec8-4ae4-82e6-538f9a98d69e)

this board was the only one where you not only have to hold the boot button while plugging in, but also have to KEEP HOLDING it until you starting flashing. then right after flashing starts you have to release the boot button.

Don't trust the "Aliexpress c3 supermini board guide" pdf for anything other than 1st, 2nd pages. the one who made it can't even write the "led fade" code example. 
here are some links that you need to visit.
https://espressif.github.io/esp32-c3-book-en/#:~:text=ESP32-C3%20is%20a%20single,effective%20solution%20for%20connected%20devices.
https://github.com/sigmdel/supermini_esp32c3_sketches?tab=readme-ov-file#02_blink_pulse_led

here is how to set up everything and upload the code to esp32-c3 supermini. 
<h2><------ SETUP ARDUINO IDE -------></h2>
	
1. select board "Adafruit QT PY ESP32-c3".
2. Go to <Tools> and set settings as below.

	1. USB CDC on boot: "Enabled"

	2. CPU Frequency:"160MHz (WIFI)"

	3. Core Debug level: "None"

	4. Erase all flash before sketch Upload: "Disabled"

	5. Flash Frequency:"80MHz"

	6. Flash mode: "QIO"

	7. Flash Size:"4MB(32Mb)"

	8. Partition scheme: "Default 4MB with spiffs(1.2MB APP/1.5MB SPIFFS)"

	9. Upload Speed:"115200"

	10. Zigbee Mode: "Disabled"

Follow the first instruction to upload the code. 
if your Code messed up with the Firmware (it happens some times when you try to use I2C Library) here is how to flash Firmware.
https://docs.espressif.com/projects/esp-at/en/release-v2.4.0.0/esp32c3/AT_Binary_Lists/ESP32-C3_AT_binaries.html

<h2><----------- I^2C Problems ----------></h2>
Don't use Default I2C pins. pin8 has on board led and it does not work. <b>use GPIO-1,GPIO-2 pins.</b>. if you can, Do a bit of research and find out a way to use some other pins.

END.
