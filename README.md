# HDD-Clock-V3.0
Hard Drive Persistence of Vision Clock V3.0  -  This will be replaced with V4.0 shortly. V3.0 had some parts that need to be moved to make the PCB better fit the HDD case. I'm also improving the power design.

This project is the third version of my Hard Drive Persistence of Vision Clock. This clock is built around a Dell MBE2147RC 2.5" HDD. The clock uses the spindle motor, frame, and 1 of the platters modified to be a spinning light mask. PCB versions of the spinning light masks are also being tested.

Here is how V2.0 turned out. V2.0 used a single slit in the light mask. V3.0 will be capable of this. I am also going to try a few different variations of the light mask to see what effects I can achieve. V2.0 Reference:

![PXL_20210112_035651076](https://user-images.githubusercontent.com/23159547/157259011-be7111de-0e63-4f6e-8234-9c51ee3db2fc.jpg)

V3.0 of this clock uses a spinning light mask with evenly spaced holes. The light mask is back-lit by APA102 Digital LEDs. The spinning light mask is indexed with an IR reflective sensor. Counting the time between indexes of the light sensor, the light mask's speed can be calculated. The location of each hole in the spinning light mask can be calculated from its position relative to the IR reflection point. Using precise timing, we can light LEDs behind our desired hole in the spinning light mask. Doing this while the hole is in the desired location in its rotation at a very fast rate can trick the eye into seeing a static image. This is called Persistence of Vision. (This new method of persistence of vision needs to be tested still)

I have designed 3 PCB light masks to test with V3.0 hardware. An 8 hole version of the light mask, a 12 hole version and a slit version equivalent to V2.0.

Improvements over V2.0
  1. Using a buffer IC to ensure the MCU is seeing proper HIGH and LOW levels from the IR reflective sensor
  2. Powered from USB-C. 
  3. Using APA102-2020 LEDs. These are 25X faster than WS2812B (Neopixels) and are 60% smaller allowing me to update faster and place more in the same space.
  4. Using several small holes in the light mask rather than 1 slit. This allows me to draw text instead of just clock hands.
  5. Elimination of wires for assembly. Power and data connections between the driver board and the LED board are passed between SMT PCB spring pins. This will simplify assembly and clean up the look.
  6. Right angle buttons and right angle encoder for human interface.
  7. Updated LED board shape aiding in heat disapation, consistent placement of the HDD data arm.

