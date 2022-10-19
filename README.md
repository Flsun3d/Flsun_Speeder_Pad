klipper: https://github.com/Flsun3d/klipper_fs

mainsail: https://github.com/Flsun3d/mainsail_fs

moonraker: https://github.com/Flsun3d/moonraker_fs

# Flash Speeder Pad Imager

**1.Note**: Flashing the imager will reset all configurations and lose all data on your pad, so this operation is only used to restore the original settings of the Speeder Pad

**2.Tool**：

  a)A TF card of at least 32 GB is required.

  b)A TF card reader.

  c)A PC，system is Windows、MacOS or Ubuntu for x86.

**3.Step**：

  a)Download this restoration imager：

  b)Download and install Raspberry Pi imager here：https://www.raspberrypi.com/software/

  c)Insert the TF card into the PC and double-click to open the imager：
  ![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/1.png)
  
  d)Select your TF card as Storage.
  
  e)Then click Write.
  
  f)Once the imager is written, turn off Speeder Pad if it is on and remove all devices plugged into the USB ports.
  
  g)Insert TF card in Speeder Pad.
  ![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/2.png)
  
  h)Turn on it，A loading bar should appear:
  ![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/3.png)
  
  i)And wait until the bar is fully charged and green, this may take several minutes (10/15 minutes)：
  ![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/4.png)
  
  j)When it's done, turn off Speeder Pad and remove the TF card.
  
  k)Turn Speeder Pad back on, it should start normally and arrive on KlipperScreen Splash Screen.
  
## SSH Connection 
```
  user: pi
  password: flsun
 
