# ShareBot XXL+ 3D Printer Firmware Update Calibrate Steps
Please read the whole tread on this page to help understand the process it takes to accomplish the Update

This Marlin firmware requires an older - Arduino-1.0.6-IDE-Windows-master software to compile and upload to the printer.
Please locate on github for this program I couldnt upload it onto this respritory.

You would need to copy the files that correlates to your printer. 
The files come with 5 different sets of configuration.h that go to different 3D Printers so chose wisely.

They are located in ShareBot XXL+ Firmware Update\Marlin-Marlin_v1\Marlin\example_configurations
Copy the files and paste them to Marlin folder - ShareBot XXL+ Firmware Update\Marlin-Marlin_v1\Marlin

Making a copy saves them as an original in-case you mess the code up when editing -

Open the Arduino-1.0.6-IDE-Windows-master - arduino.exe
And Open Marlins File @ - ShareBot XXL+ Firmware Update\Marlin-Marlin_v1\Marlin\Marlin.ino within arduino
to load the firmware bundle pack that you will be uploading to the printer via Mini USB cable.
The 3D Printer has a port in the front its a Mini USB cable and looks kinda funny but it fits.

Make sure to adjust the settings in Arduino to accept the ShareBot XXL+ 3D Printer
In the tools tab click Board & Select - Arduino Mega 2560
&
In the tools tab click Port & Select - which ever one the printer is connected to. Example COM? ?=A number that is per-selected for your connected device.

After you have connected the printer you can press Upload it will take about 1 minute and you'll see the printers screen go blank or have black cubes its doing its thing.

Calibrating the AXIS steps per mm #- (Optional)
See if the Stepper motors are calibrated correctly, in here you can adjust the steps per mm on the Configuration.h tab
After you measure with calipers making the printer head travel 100mm to see if in real life measurements are correct.
After you find out the numbers you can adjust accordingly.

Scroll down 3/4 of the page on the Configuration.h tab, you will see a section called "// default settings" and it will look like this.

``
// default settings

#define DEFAULT_AXIS_STEPS_PER_UNIT {80,80,400,96.2753} // default steps per unit for ultimaker

#define DEFAULT_MAX_FEEDRATE {300, 300, 12, 35} // (mm/sec)

#define DEFAULT_MAX_ACCELERATION {2000,2000,50,2000} // X, Y, Z, E maximum start speed for accelerated moves.
``

Changing the #define DEFAULT_AXIS_STEPS_PER_UNIT {80,80,400,96.2753} numbers here, will change the steps per mm
This formula is used in the (numbers of brackets ) above as (X, Y, Z, E) AXIS

JUST BE CAREFUL not to change the settings to much.

Example: I had to change my (Y) AXIS to 89 to make it a true 100mm travel. 

Each printer is different so try the best for yours.

After your desired changes press upload again and it will add the changes.

The files included will provide options to rewrite/restore/update the 3D Printer to the most resent firmware that ShareBot and its partners created.
The newest version says "Sharebot XXL2" on the display of the printer and that is when you'll know that it has been updated.
Old firmware says "ShareBot XXL+"
I had some trouble finding the firmware so I figured, others might have an issue with it as well so I created this stream on GITHUB.

There is another .exe software in the files that I will provide to help with less coding capable people. The ShareBot company sent me these ones personally but I was not able to try them out yet since I already updated my printers firmware. Use this one at your own risk I cant be responsable for you bricking your printer. I didnt brick mine but its always possible.

I hope this helps if you can leave a review on my website or googles listing it would help me get to help more people that are in search of services and solutions.

TOA3DPRINTING on google 
