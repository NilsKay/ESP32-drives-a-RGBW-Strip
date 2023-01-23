# ESP32-drives-a-RGBW-Strip
Connect ESP32 and a RGBW strip with sk6812 controller 

Using Pin32 as the LED bus Pin. This repro is build around the adafruit neopixel library, using a modified
example (RGBWStrandtest) from that library. I used a ESP32 WROOM NodeMCU as uc controller
I use this to test a led-strip, or only parts of a strip. Even a single led will work.

Right now it is set to drive 40 LED's. I disabled all the rainbow etc. effects since I only want to test if the led's work properly.
The need for this came when after half a year of working fine suddenly a 60 LED's strip (Used as a TV backlight) started to flicker or not turning on at all. 
Only the LED's 10-60 were affected, 1 to 9 worked fine.
So I took that strip to my workbench cut it into sections and tested with this sketch. 
The result was, that 20 out of the 60 LED's were damaged beyond hope, randomly distributed along the strip. Even when only one of the damaged LED's was connected, it just flickered randomly. So no power or strip length problem can be the reason. Undamaged sections work like a charm, so also no timing problem.

My conclusion: For some unknown reason the controller chips on the damaged Leds are fried...

