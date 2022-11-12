klipper: https://github.com/Flsun3d/klipper_fs

mainsail: https://github.com/Flsun3d/mainsail_fs

moonraker: https://github.com/Flsun3d/moonraker_fs

1. If  the SpeederPad does not work properly during the process of upgrading or modifying it, you can try to use the method in this tutorial to re-flash the image .

2. If you need to make some upgrades and your own modifications to the PAD, we strongly recommend making modifications in our published image system to ensure compatibility in later versions.

3. For the security of your system, it is recommended that you change the password in time after downloading and flashing the image. If you do not need to modify the system, it is recommended that you close the SSH service. Enter "sudo systemctl disable ssh" in SSH and restart it to take effect.

## Table of Tutorial

- [Flash Speeder Pad Imager](#flash-speeder-pad-imager)
- [Connect to the network](#connect-to-the-network)
- [SSH Connection](#ssh-connection)
- [Change password](#change-password)
- [Update the firmware](#update-the-firmware)
- [How to use Timelapse](#how-to-use-timelapse)
- [Building and flashing the micro-controller](#building-and-flashing-the-micro-controller)
- [Upload configuration to Speeder Pad](#upload-configuration-to-speeder-pad)


## Flash Speeder Pad Imager

**1.Note**: Flashing the imager will reset all configurations and lose all data on your pad, so this operation is only used to restore the original settings of the Speeder Pad

**2.Tool**：

  a)A TF card of at least 32 GB is required.

  b)A TF card reader.

  c)A PC，system is Windows、MacOS or Ubuntu for x86.

**3.Step**：

  a)Download this restoration imager：https://drive.google.com/file/d/1-CcpLf8EmEKliuO_8VQEuspvWL6l8QFh/view?usp=sharing

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

## Connect to the network 

**a)When the printer is not connected**

1.When the following interface appears on the printer, please wait for the connection to time out, usually about 1 minute.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/5.png)

2.Click the "Menu" button at this time, the following interface will appear, please click the "Return" button and wait patiently.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/6.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/7.png)

3.Please proceed to the next step until the following interface appears.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/8.png)

4.click the "menu" button to enter the "Network" option to configure the network.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/9.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/10.png)

5.The connected WIFI needs to be in the same local area network as the computer, tablet or mobile phone to control the Speeder Pad.

6.After selecting the right button of the WIFI you want to connect. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/11.png)

7.enter the password of this WIFI and click the "Save" button to save.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/12.png)

8.When prompted with the following screen, click the "Close" button to close the page and return to the "Network" menu.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/13.png)

9.If it is the first time to connect, please wait for a while. If the IP cannot be displayed, you can click the "Refresh" button in the upper right corner to refresh the address. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/14.png)

10.If the screen still displays "IP: 0.0.0.0" after clicking the "Refresh" button.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/15.png)

11.Please click the "Return" button, then click the "System" page.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/16.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/17.png)

12.After clicking the "System Restart" button, click the "Continue" button to restart the Speeder Pad system.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/18.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/19.png)

13.When the printer displays the following interface after restarting, please wait for the connection to time out, usually about 1 minute.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/20.png)

14.At this point, click the "Menu" button, the following interface will appear, please click the "Return" button and wait patiently.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/21.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/22.png)

15.When this page appears, proceed to the next step.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/23.png)

16.click the "menu" button to enter the "Network" option to configure the network.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/24.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/25.png)

17.After the connection is successful, an IP address will be generated, and you can access this IP address through a browser to print online. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/26.png)

18.If the IP still cannot be displayed after restarting, please try restarting the Speeder Pad again, restarting the router or connecting to another router.

19.If the IP still cannot be displayed after restarting the router, please check that the DHCP service is enabled on your router.

20.Use the computer, tablet or mobile phone in the same local area network which the Speeder Pad is connected,enter ：http:// ********* in the URL bar of the browser (IP of the Speeder Pad: the displayed IP address).
   Here is: http: //192.168.1.18 (for example）；If you enter the correct IP, the following page will appear, indicating that the network has been successfully connected.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/27.png)


**b)With the printer connected**

1.click the "Configuration" button to enter the "Network" option for network configuration. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/28.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/29.png)

2.The connected WIFI needs to be in the same local area network as the computer, tablet or mobile phone to control the Speeder Pad.

3.After selecting the right button of the WIFI you want to connect. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/30.png)

4.Enter the password of this WIFI and click the "Save" button to save.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/31.png)

5.When prompted with the following screen, click the "Close" button to close the page and return to the "Network" menu.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/32.png)

6.If it is the first time to connect, please wait for a while. If the IP cannot be displayed, you can click the "Refresh" button in the upper right corner to refresh the address. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/33.png)

7.If the screen still displays "IP: 0.0.0.0" after clicking the "Refresh" button.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/34.png)

8.Please click the "Back" button.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/35.png)

9.Then click the "System" page.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/36.png)

10.After clicking the "System Restart" button, click the "Continue" button to restart the Speeder Pad system.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/37.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/38.png)

11.After restarting the system,click the "Configuration" button to enter the "Network" option for network configuration.  
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/39.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/40.png)

12.After the connection is successful, an IP address will be generated, and you can access this IP address through a browser to print online. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/41.png)

13.If the IP still cannot be displayed after restarting, please try restarting the Speeder Pad again, restarting the router or connecting to another router.

14.If the IP still cannot be displayed after restarting the router, please check that the DHCP service is enabled on your router.

15.Use the computer, tablet or mobile phone in the same local area network which the Speeder Pad is connected,enter ：http:// ********* in the URL bar of the browser (IP of the Speeder Pad: the displayed IP address).
   Here is: http: //192.168.1.18 (for example）
If you enter the correct IP, the following page will appear, indicating that the network has been successfully connected.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/42.png)


## SSH Connection 
```
  user: pi
  password: flsun
```

1.Before connecting, please make sure that the computer you want to operate is in the same local area network as the Speeder Pad, and can normally access the Speeder Pad control page through a browser.

2.Download and install MobaXterm software from this link: https://mobaxterm.mobatek.net/download-home-edition.html

3.Here we recommend downloading the "Portable edition" version.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/43.png)

4.After starting the software, click the "Session" button.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/44.png)

5.Click the "SSH" button,enter the IP address of your Speeder Pad in the "Remote Host" field, check "Specify username", enter "pi" and click the "OK" button to complete the SSH setup.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/45.png)

6.On the new displayed window, enter the password in the new window (the password is not displayed when typing, this is normal): 
flsun
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/46.png)

7.An authorization window will appear, authorize it. There may also be another window asking you to change your password, please ignore it, click the "No" button. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/47.png)

8.After connecting, on the left side of the window, you can access and modify the folders and files for uploading and downloading Speeder Pad, and on the right side access the SSH command prompt window:
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/48.png)


## Change password

1.Since the initial password of the PAD is the same,if you use it for the first time,it is recommended that you change the password.

2.Enter the following command in the SSH command prompt window: 
```
  sudo passwd pi
```
3.The system will ask you to enter the current password for verification, please enter: 
```
  flsun
```
4.Verification is complete, you can enter a new password and press Enter to confirm.

5.NOTE: When entering the password, for the security of the password, you will not be able to see any characters in the window. Please ignore it. Just enter the password and click Enter.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/49.png)

6.After successfully verifying the password, it will be applied immediately.

## Update the firmware

1.If you need to install or re-update the Klipper firmware while your printer is connected to PAD.

2.We provide some compiled firmware, available from here: https://github.com/Flsun3d/Flsun_Speeder_Pad/tree/main/firmware
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/50.png)

3.Select the firmware of the corresponding machine model, download and open the folder where it is located, such as "SR".
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/51.png)

4.After entering the folder, there is usually a "read me" file that tells you how to use it. You can download the firmware that matches your motherboard chip according to the instructions.

5.Please pay attention to the instructions in the folder, please follow the instructions in the folder to download the firmware used, click the file with the suffix .bin and then click the "Download" button to download.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/52.png)

6.Prepare a TF card and insert it into the computer.

7.The TF card needs to be formatted as FAT32 and the allocation size is 4096.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/53.png)

8.After downloading, copy all the files in the folder to the root directory of the TF card.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/54.png)

9.Safely remove the TF card and insert it into the motherboard, then turn on the printer. 

10.It only takes a few seconds to install, then pull out the TF card after power off.

11.Usually after the firmware is successfully flashed, the original screen does not work.

12.Usually, after the firmware is installed successfully, the file with the “.BIN “ in the TF card will become the “.CUR “.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/55.png)


## How to use Timelapse

**a)Cura software settings**

1.Open the Cura software, click Extension - Post Processing - Modify G-CODE. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/56.png)

2.Click to add a script, select "Insert at layer change". 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/57.png)

3.Select "Before" in the "When to insert" option, fill in "TIMELAPSE_TAKE_FRAME" in "G-code to insert", and click "Close".
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/58.png)

4.If you need to output video after every printing, add "TIMELAPSE_RENDER" to the end code of G-code. Click on "Settings-Printer-manage Printers".
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/59.png)

5.Click "Printer", select your printer model, and click "Machine Settings". 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/60.png)

6.Add "TIMELAPSE_RENDER" to the end code and click "Close". 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/61.png)

7.When the Pad is turned on, insert the camera into the USB port on the right side of the Pad.

**b)Web page settings**

1.When the Pad is turned on, insert the camera into the USB port on the right side of the Pad.

2.Connect to WIFI, enter the generated IP address into a browser on the same local area network.Click the button in the upper right corner of the webpage, as shown below.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/62.png)

3.Click the refresh button of "Webcamb". As shown below.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/63.png)

4.If you want to set the time-lapse camera mode, click the button in the upper right corner of the webpage, as shown below.  
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/64.png)

5.Click "TIMELAPSE" and select the mode you want. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/65.png)

6.For example: If you want to set the nozzle position,movement speed and distance, you can check "Park Toolhead".
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/66.png)

**c)How to print with Timelapse.**

1.Save the Gcode file to your computer.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/67.png)

2.On the webpage, click "G-CODE FILES" and the upload button to upload the G-CODE file to the webpage.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/68.png)

3.Right-click on the G-CODE file and click "Print start".
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/69.png)

4.After the timelapse configuration is successful, click the Gcode file, and “Timelapse” will be prompted in the pop -up box.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/70.png)

5.Click "Webcam" on the home page to monitor your printer in real time.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/71.png)

6.After printing, the video will be automatically saved in "TIMELAPSE" bar.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/72.png)

7.Right-click the file and click Download.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/73.png)


## Building and flashing the micro-controller

1.We provide compiled firmware, but because there are many types of printers and motherboards, if your printer is not in the preset configuration, you can try to configure the firmware yourself to make Speeder Pad connect to your printer.

2.In the SSH command prompt window, enter the following commands (input one at a time):
```
  cd ~/klipper/
  make menuconfig
```
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/74.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/75.png)

3.You can contact the company of your motherboard or printer to get the Klipper firmware configuration parameters of your printer, or you can find it through this link:
 https://github.com/Klipper3d/klipper/tree/master/config
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/76.png)

4.Please contact your printer, motherboard supplier or search the Internet to obtain the chip information of your printer, motherboard and motherboard, and then search for the corresponding configuration file.

5.Taking "Flsun-Q5" as an example, click the "printer-flsun-q5-2020.cfg" file on the left to view the file.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/77.png)

6.The comments at the top of the printer configuration file describe the settings that need to be set during "make menuconfig". Open the .cfg file in the web browser or text editor, and find these comments near the top of the file. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/78.png)

7.Select parameters such as chip structure, chip model, Bootloader offset, external clock, communication port, etc.
(Please follow the motherboard configuration)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/79.png)

8.On the lower right side of the screen are the operating instructions for the compilation environment.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/80.png)

9.You can use the "direction key" to move up and down, use the "Space/Enter" key to select and confirm, and use the "ESC" key to return or exit.

10.The chip used can be found according to the documentation notes: STM32F103
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/81.png)

11.In MobaXterm software, click the command prompt window on the right side of the screen, and use the arrow keys to move down, as shown in the figure. Then use the "Space/Enter" key to select and enter the next menu.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/82.png)

12.When the following screen appears, use the arrow keys to move down four times, select the menu as shown in the figure, and then use the "Space/Enter" key to confirm.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/83.png)

13.After the selection is successful, you should return to the menu as shown in the figure. At this time, use the arrow keys to move down, and use the "Space/Enter" key to select and enter the next menu.

14.Then select the "STM32F103" option and confirm with the "Space/Enter" key.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/84.png)

15.This will return to the main menu and the chip configuration section is complete.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/85.png)

16.Enable the "extra low-level" feature as noted in the documentation.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/86.png)

17.Use the arrow keys to move up once, select the menu as shown in the figure, and then use the "Space/Enter" key to confirm the selection and enable the "extra low-level" function.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/87.png)

18.Set Bootloader to 28KiB according to the documentation.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/88.png)

19.Use the arrow keys to move down four times, select the menu as shown in the figure, and use the "Space/Enter" key to select and enter the next menu.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/89.png)

20.Use the arrow keys to move down twice, select "28Kib bootloader" and then use the "Space/Enter" key to confirm the selection.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/90.png)

21.You will now be returned to the main menu and the Bootloader configuration section is complete.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/91.png)

22.Set up Serial (on USART3 PB11/PB10) as noted in the documentation.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/92.png)

23.Use the arrow keys to move down twice, select the menu as shown in the figure, and use the "Space/Enter" key to select and enter the next menu.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/93.png)

24.Use the arrow keys to move down four times to the “(on USART3 PB11/PB10)” menu as shown in the figure, and use the “Space/Enter” key to confirm the selection.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/94.png)

25.This will return to the main menu, and the serial port configuration part is complete.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/95.png)

26.The parts not mentioned in the configuration instructions do not need to be configured, just follow the default.

27.After the parameter configuration is completed, press "Q" to save, and then press "Y" to confirm.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/96.png)

28.If the comments at the top of the printer configuration file describe special steps for "flashing" the final firmware image to the printer control board, then follow those steps.

29.The steps of burning are mentioned in the configuration file, and we should follow the steps of the configuration file.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/97.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/98.png)

30.Start compiling the firmware by entering the following commands:
```
  make
```

31.Find the location where the firmware is stored.

32.Find the firmware in the "/home/pi/klipper/out/" directory obtained on the left side of the MobaXterm software. 
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/99.png)

33.Run the mentioned command at the command prompt as instructed by the configuration documentation.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/100.png)

34.Start compiling the firmware by entering the following commands:
```
  ./scripts/update_mks_robin.py out/klipper.bin out/Robin_nano.bin
```
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/101.png)

35.Prepare a TF card and insert it into the computer.

36.The TF card needs to be formatted as FAT32 and the allocation size is 4096.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/102.png)

37.Download and copy "Robin_nano.bin" to the TF card according to the instructions of the configuration file.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/103.png)

38.Find the downloaded file on the left side of the MobaXterm software, right-click to select "Downlad", and then click the left-click to download the file to the root directory of the just formatted TF card.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/104.png)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/105.png)

39.Safely remove the TF card and insert it into the motherboard, then turn on the printer. 

40.It only takes a few seconds to install, then pull out the TF card after power off.

41.Usually after the firmware is successfully flashed, the original screen does not work.

42.Usually, after the firmware is installed successfully, the file with the “.BIN “ in the TF card will become the “.CUR “.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/106.png)

43.If your motherboard has no BootLoader and is not an SD card upgrade, please use the following method to upload the firmware.

44.Please unplug all connected devices from the USB port on the Speeder Pad first. 

45.Connect the printer to the "Port1" USB port of Speeder Pad with a USB cable. Please keep connection during the firmware upgrade.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/107.png)

46.In the SSH command prompt window, enter the following commands (input one at a time):
```
  cd ~/klipper/
  make menuconfig
```

47.The following steps can refer to the content of steps 3-26 in this part of the tutorial.

48.Select parameters such as chip structure, chip model, Bootloader offset, external clock, communication port, etc.
(Use mega2560 as a demonstration, please follow the motherboard configuration)
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/108.png)

49.After the parameter configuration is completed, press "Q" to save, and then press "Y" to confirm.
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/109.png)

50.Start compiling the firmware by entering the following commands (input one at a time):
make clean
make
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/110.png)

51.Enter the following command to start getting serial port information:
```
  ls /dev/serial/by-id/*
```

52.It should report something like:
```
  /dev/serial/by-id/usb-1a86_USB_Serial-if00-port0
```
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/111.png)

53.For common microcontrollers, the firmware can be flashed using something like the following (input one at a time):
```
  service klipper-1 stop
  make flash FLASH_DEVICE=/dev/serial/by-id/usb-1a86_USB_Serial-if00-port0
  service klipper start
```

54.Be sure to update the FLASH_DEVICE parameter with the printer's unique serial port name.

55.Upgrade has been completed:
![image](https://github.com/Flsun3d/Flsun_Speed_Pad/blob/main/image/112.png)


## Upload configuration to Speeder Pad

1.Create a new folder and rename the folder to "Printer Model + Size + Leveling Method",For example Flsun-Q5, the size is 200*200*200, and the leveling method is Autolevel, then the folder name is "Flsun-Q5 pro 200*200*200 Autolevel".

2.The folder contains two files, one is firmware, usually ending with .bin, and the other is printer.cfg. Please write the options for compiling firmware at the beginning of printer.cfg, for example:
```
    # This file contains common configurations and pin mappings
    # for the Flsun Q5 using the MKS Robin Nano board.
    # To use this config, the firmware should be compiled for the
    # STM32F103. When running "make menuconfig", enable "extra low-level
    # configuration setup", select the 28KiB bootloader, and serial (on
    # USART3 PB11/PB10) communication.
    # Note that the "make flash" command does not work with MKS Robin
    # boards. After running "make", run the following command:
    # ./scripts/update_mks_robin.py out/klipper.bin out/Robin_nano.bin
    # Copy the file out/Robin_nano.bin to an SD card and then restart the
    # printer with that SD card. 
```

3.Compress this folder and send it to the specified mailbox:flsun_email@163.com

4.We will publish to Speeder Pad library after reviewd.
 
