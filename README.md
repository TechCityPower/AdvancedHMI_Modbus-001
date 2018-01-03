# AdvancedHMI_Modbus-001
The first glance at the AdvancedHMI panel project. Modbus communication test.

--- http://advancedhmi.com/forum/index.php?topic=666.0
Here is how to run an AdvancedHMI application on a Raspberry Pi

1) Download the Debian Wheezy image
http://www.raspberrypi.org/downloads/

2) Copy the image to the MicroSD card using Win32DiskImager
3) Install the card and boot up the Pi
4) When it gets to the configuration screen, set it to expand the image and also to boot to a Graphical User Interface
5) Select Finish in the configuration and Reboot
6) Once booted into the GUI, open a Command Prompt
7) Type these series of commands:

sudo su
apt-get update
apt-get install mono-complete
apt-get install mono-vbnc

8 ) Put in a memory stick with an AdvancedHMI application on it
9) In the command prompt, use the "cd" command to browse to the memory stick to the directory /bin/debug
10) mono AdvancedHMI.exe

In a few seconds the application should start.

There are a few things you may run into. 

- You cannot use an OPC server because it is not a .NET application
- The MessageDisplayByValue may stop the application because it uses a speech library. There is a work around. Find System.Speech.DLL on your Windows PC and copy the file into the /bin/debug directory
