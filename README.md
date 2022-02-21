# HDD-Clock-V3.0
Hard Drive Persistence of Vision Clock V3.0

This project is the third version of my Hard Drive Persistence of Vision Clock. This clock is built around a Dell MBE2147RC 2.5" HDD. The clock uses the spindle motor, Case, and 1 of the platters modified to be a spinning light mask. PCB versions of the spinning light masks are also being tested.

This clock uses a spinning light mask with evenly spaced holes. The light mask is back-lit by APA102 Digital LEDs. The spinning light mask is indexed with an IR reflective sensor. Counting the time between indexes of the light sensor, the light mask's speed can be calculated. The location of each hole in the spinning light mask can be calculated from its position relative to the IR reflection point. Using precise timing, we can light LEDs behind our desired hole in the spinning light mask. Doing this while the hole is in the desired location in its rotation at a very fast rate can trick the eye into seeing a static image. This is called Persistence of Vision.

The current plan is to have at least 8 dots or "pixels" tall in the spinning light mask. If I can add an additional 6 dots placed precicely between the first 7 dots I can make a solid line out of the dots. If possible, worth experimenting with. The spinning light mask will likely be 3D printed.

Improvements over V2.0
  1. Using a buffer to ensure the MCU is seeing proper HIGH and LOW levels from the IR reflective sensor
  2. Powered from USB-C. 
  3. Using APA102-2020 LEDs. These are 25X faster than WS2812B (Neopixels) and are 60% smaller allowing me to update faster and place more in the same space.
  4. Using several small holes in the light mask rather than 1 slit. This allows me to draw text instead of just clock hands.
  5. Elimination of wires for assembly. Power and data connections between the driver board and the LED board are passed between SMT PCB spring pins. This will simplify assembly and clean up the look.
  6. Right angle buttons and right angle encoder for human interface.
  7. Updated LED board shape aiding in heat disapation, consistent placement of the HDD data arm.

