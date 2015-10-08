# ZYBOT
zybo tank/robot
-----still in progress----
software & tricks to make zybo tank work:

To get linux on zybo:
download "USB Image Tool": http://download.cnet.com/USB-Image-Tool/3000-2242_4-75449768.html
download "Xillinux": http://xillybus.com/downloads/xillinux-1.3.img.gz
download "xillinux bootfiles": http://xillybus.com/downloads/xillinux-eval-zybo-1.3c.zip

Run USB Image TOOL, select your SD card as target device, select restore, locate your xillinux-1.3.img.gz file, make sure the drop down menu is set to "all files" or ".img.gz" files.Select your file and let the USB Image Tool run this will create the propper partitions and file systems. 
After this is done, copy the files from the "COPY_TO_BOOT" directory in the only partition of your SD card that should be visible to windows, it is possible that this partition is very small, around 16MB.

optional:
if you would like to generate your own .bit file, follow this guide(for vivado it start at 3.5.2): http://xillybus.com/downloads/doc/xillybus_getting_started_zynq.pdf    (this guide can also help you with the other steps, I have just tried to condens and simplify it)
You can also find the other boot files in the .zip file (xillinux-eval-zybo-1.3c.zip) in the boot directory.
-end of optional

After this you should have 4 files in your boot partition, and you can now put the SD card in the ZYBO and it should be able to boot off of it, make sure the jumper on the zybo is set to SD.


SOFTWARE: install libfreenect ( use manual install)
http://openkinect.org/wiki/Getting_Started

FIX:Undefined reference to libusb_get_parent() , while compiling freenect
http://stackoverflow.com/questions/28835794/undefined-reference-to-libusb-get-parent-compiling-freenect
