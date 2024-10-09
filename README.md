# ESP32-C3SUPERMINI
Guide to use ESP32-C3 Supermini board that you Bought From Aliexpress

this board was the only one where you not only have to hold the boot button while plugging in, but also have to KEEP HOLDING it until you starting flashing.

Don't trust the "c3 supermini board guide" pdf for anything other than 1st, 2nd pages. the one who made it can't even write the "led fade" code example. 

<------ SETUP ARDUINO IDE ------->
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

END.
