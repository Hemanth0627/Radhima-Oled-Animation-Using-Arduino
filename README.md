RADHIMA UNO OLED TEST

Files in this folder:
- RadhimaUnoTest.ino: Arduino sketch
- animation_uno_sample.h: 15 sampled 128x64 frames and their timing

Setup:
1. Install the Adafruit SSD1306 and Adafruit GFX libraries in Arduino IDE
   (Sketch > Include Library > Manage Libraries).
2. Connect OLED VCC to Uno 5V, GND to GND, SDA to A4, and SCL to A5.
3. Open RadhimaUnoTest.ino from this folder. Keep animation_uno_sample.h beside it.
4. In Arduino IDE select Tools > Board > Arduino AVR Boards > Arduino Uno.
5. Select the Uno's port under Tools > Port, then click Upload.

This reduced test keeps original frames 0, 15, 30, ... 210. It combines
original frame durations between samples so the full animation cycle remains
22.2 seconds. Original bitmap bytes and 128x64 dimensions are unchanged.
The animation data is 15,360 bytes; the smaller frame set leaves more Uno
program storage for the display libraries and sketch.
