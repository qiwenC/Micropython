# Installation

1.  Install [Anaconda](www.continuum.io).

2.  Install [Pymark](https://www.pycom.io/solutions/pymakr).

# Connection to the Wipy board and a little test.

1.  Look for the reset button on your module (located at a corner of the board).
  Look for the USB connector on your expansion board.
  Insert the module on the expansion board with the reset button pointing in the same direction as the USB connector.
  
2. Plug the board into any powered USB cable (computer or a battery charger).

  In a few seconds, the LED should start blinking every 4 seconds. If it isn't blinking,  disconnect the power supply and re-check the boards position on the expansion board.
  
3.  Initial configuration. 
>1. Connect the computer to the WiFi network named after your board (e.g. lopy-wlan-xxxx, wipy-wlan-xxxx). The password is www.pycom.io
>2. Open Pymakr.
>3. In the menu, go to Settings > Preferences (Pymakr > Preferences on macOS).
>4. In the left list look for Pycom Device.
>5. For device, type down 192.168.4.1. The default username and password are micro and python, respectively.
>6. Click OK

4.  Testing
 
    Create a new file and type in the codes.
   
   ```
   import pycom
   import time 
   pycom.heartbeat(False)   
   for cycles in range(10): # stop after 10 cycles    
   pycom.rgbled(0x007f00) # green    
   time.sleep(5)  
   pycom.rgbled(0x7f7f00) # yellow   
   time.sleep(1.5)
   pycom.rgbled(0x7f0000) # red    
   time.sleep(4)
   ```
