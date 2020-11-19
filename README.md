# underwater-assembly-auv
Repository containing parts list and CAD files to retrofit a BlueROV2 for improved autonomous operation. The starting point would be a BlueROV2 heavy. A CAD file of the build is available [here](https://www.dropbox.com/s/99sjkslvtko1nd0/Electronics.igs?dl=0). Note that the front mounting plate is different than what is in that CAD file. I was experimenting with adding fans for camera cooling. What I use now in the robot is represented in the dxf file below.

The DXF files are usable as laser cutting patterns. The files `Electronics Tray Body.dxf`, `Electronics Tray Body.dxf`, and `rear electronics tray mount.dxf` are cut from 4.9mm delrin plastic from ponoko.com

The file `Camera Mount.dxf` is cut from 3.2mm black delrin from ponoko.

The file `FCU Mount.dxf` is cut from 2mm aerospace aluminum from send cut send.

The hardware for assembling the components comes from mcmaster-carr and allied electronics (for the mounting brackets). See the packing lists for both of those orders for details on the components.

# Electronics

ESCs: 2x DALRC rocket 50a from [here](https://www.getfpv.com/dalrc-rocket-50a-3-6s-blheli-32-4-in-1-esc.html). You also need another FCU to configure the ESCs. We use the DALRC f722 dual from [here](https://www.banggood.com/DALRC-F722-DUAL-STM32F722RGT6-F7-Flight-Controller-MPU6000-and-ICM20602-Built-in-OSD-for-RC-Drone-p-1346923.html?utm_source=google&utm_medium=cpc_ods&utm_campaign=arvin-cam-sds-view-tent-content&utm_content=arvin&gclid=EAIaIQobChMIp-L2zNah6gIVja_ICh15_QWHEAAYASAAEgIs4vD_BwE&cur_warehouse=CN)

Main computer: UpBoard UpSquared [here](https://up-board.org/upsquared/specifications/). We use the 8GB ram quad core model
Main computer addons:
  * UpSquared wifi kit [here](https://up-shop.org/m-2-2230-wifi-kit-wifi-802-11-ac-2t2r-for-up-squared-metal-chassis.html) used to connect to the robot when it is on the surface
  * SSD for the upboard. We use [this one](https://www.amazon.com/gp/product/B07GZLJD5R/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
  * Tiny USB 2 cable for connecting to FCU [here](https://www.amazon.com/gp/product/B01NAMTC5T/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
  * Locking but small USB 3 cable for connecting to the camera [here](https://www.usbfirewire.com/parts/rr-armsk-xxgr.html#RR-ARMSK-12GR)
  
FCU: An Mrobotics X2.1. It is a smaller clone of the pixhawk with updated sensors. Available [here](https://store.mrobotics.io/mRo-X2-1-Rev-2-p/mro-x2.1rv2-mr.htm). We ordered with all cable options. Essential is the bridge cable for usb2.0 connection.

Power management:
  * Blue robotics underwater switch for the relay [here](https://bluerobotics.com/store/comm-control-power/switch/switch-10-5a-r1/)
  * 80A car relay. We used [this](https://www.amazon.com/gp/product/B00RX11KLW/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
  * 2x ZTW BECs [here](https://www.amazon.com/gp/product/B071CHGWRM/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1). One powers the FCU and the other the upboard
  * 60A boat fuse [here](https://www.amazon.com/gp/product/B0000AXYEO/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1). Protects against runaway loops in control or firmware causing components to burn out.
  * 2.1mm barrell connector for UpSquared [here](https://www.amazon.com/gp/product/B081TV7SQ7/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
  
Camera:
  * FLIR Blackfly S U3 Model: BFS-U3-16S2M-CS: 1.6 MP, 226 FPS, Sony IMX273, Mono [here](https://www.flir.com/products/blackfly-s-usb3/?model=BFS-U3-16S2M-CS)
  * Lense: Stardot technologies LEN 3.5mm CS [here](http://stardot.com/megapixel-lenses)

# Other hardware

The mounting hardware order from McMaster has most of what you need. In addition to that, you need:

* I use velcro straps rather than zip ties [here](https://www.amazon.com/gp/your-account/order-history/ref=ppx_yo_dt_b_search_od?ie=UTF8&ij=&opt=ab&ref_=&search=112-1121929-5260201). The rectangular  holes on the mounting plate are designed to allow you to feed the velcro through the plate allowing you to mount custom payloads easily.
* Aluminum hex standoffs to accomodate for the longer body plate are needed. Four of [these](https://www.mcmaster.com/98952A108/) and two of [these](https://www.mcmaster.com/98952A118/)
* A pack of vibration damping standoffs for the FCU: [here](https://www.amazon.com/gp/product/B082ZNTKXT/ref=ppx_yo_dt_b_search_asin_image?ie=UTF8&psc=1)
* Vibration damping washers for mounting below the camera. I also put these washers between the thrusters and the vehicle's body: [here](https://www.amazon.com/gp/product/B077B5PPMQ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
* 4 of steel corner brackets for mounting the camera plate: [here](https://www.alliedelec.com/product/keystone-electronics/4336/70181667/?referrer=search)
* For my current build, I use mr30 connectors to bridge between the ESC's output wires and the penetrators. I think it would be better to use regular bullet connectors instead of these though: [here](https://www.amazon.com/gp/product/B0711XJ3Q2/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
* Upgrading to the cobalt connector-ized thrusters was a big lifestyle improvement. I use the cobalt connectors whenever I can: https://www.bluetrailengineering.com/product-page/blue-robotics-t200-thruster-with-cobalt-connector
* I use high flexibility silicone wire everywhere inside the tube. It packs better than standard wire and is supposed to stand up better to vibration than standard wire. I used various sizes of this brand: [here](https://www.amazon.com/BNTECHGO-Silicone-Flexible-Resistant-Insulation/dp/B018H1BDP4/ref=pd_day0_23_1/146-2345653-4128354?_encoding=UTF8&pd_rd_i=B018H1BDP4&pd_rd_r=cafb2983-5c39-4335-8fcb-0022308be669&pd_rd_w=NUnrJ&pd_rd_wg=tu8oQ&pf_rd_p=ecf748b5-e796-4a0d-9a46-406a973ba8da&pf_rd_r=4QPC3SEZKFXJTSN7T173&psc=1&refRID=4QPC3SEZKFXJTSN7T173)


# Notes

* The ESC->penetrator connections are tough to fit in. You need to solder the ESC's wires at 90 degrees to the ESC body
* I use this brand of silica gel packet [here](https://www.amazon.com/gp/product/B01LZAQPEY/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1). Because of how warm it can get in the tube when the UpSquared is churning, silica descicant is necessary in the main electronics tube.
* The wifi setup I use as the virtual tether makes the upboard unable to connect to the internet. To make life easier I run one of [these](https://www.amazon.com/gp/product/B01IQWGKQ6/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) ethernet cables into the camera compartment so I can easily jack the robot into the internet. I keep an ethernet cable with a junction like [this](https://www.amazon.com/gp/product/B016B13U9Y/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) handy.
* If you want to run the robot with a tether, you will need to find a place to put the fathom-X board (the tether interface board) and to connect it to an ethernet jack on the UpBoard. There should be a good spot for doing this below the UpBoard's heatsink on the underside of the electronics board.

# Software setup

## TODO flesh this out

Install SimpleSub on the FCU. The source code for SimpleSub can be found here https://gitlab.com/dartmouthrobotics/ardupilot-simplesub. Instructions for building and uploading coming soon.

Install Ubuntu 18.04 server on the UpSquared, ensuring that it is booting from the SSD and not the EMMC memory that comes with the board. Install ROS melodic.


## Building & Installing the SimpleSub FCU firmware 

The FCU runs a custom built Ardupilot firmware that I call SimpleSub. SimpleSub can be found here: https://gitlab.com/dartmouthrobotics/ardupilot-simplesub/-/tree/SimpleSub-v0.0.1 

Clone that repository and ensure you are on the SimpleSub branch. Once you have done so, run the environment setup script that ardupilot provides by picking the right script from this directory for your OS https://gitlab.com/dartmouthrobotics/ardupilot-simplesub/-/tree/SimpleSub-v0.0.1/Tools/environment_install 

After that is done, you need to reload your environment: source ~/.bashrc (if on linux) 

With that, you should be able to build the code with the following commands from the ardupilot directory: 

./waf configure –board=mRoX21 

./waf build –targets=simplesub/SimpleSub 

Adding the –upload option onto the waf build command should upload the firmware to the FCU if the FCU is plugged in to your computer via a usb connection, but this doesn’t work for me. What works is running QGroundControl and then plugging the FCU into the computer and using that GUI to upload the custom firmware. The waf build command above will put a file called “simplesub.apj” into the “bin” folder. In the QGroundControl GUI, select the upload custom firmware option and select “simplesub.apj”. This should work! 

Another option for uploading the firmware that works for me is: 

./waf --upload --targets simplesub/SimpleSub --upload-port /dev/ttyACM0 (I found the device descriptor /dev/ttyACM0 by looking at dmesg) 

In addition it can be built and uploaded simultaneously like so: 

./waf build --upload --targets simplesub/SimpleSub --upload-port /dev/ttyACM0 

It looks like the issue with this was that when the device is rebooted by the firmware uploader script, it gets a different device id. The firmware uploader correctly found the first usb serial device (look at /dev/serial/by-id to find the one), but when it is booted in firmware mode, it got a different id. 

This command should be easier to replicate and it worked. The first usb serial device is the one that shows normally, and the second is the one after trying to run the firmware uploader: 

./waf build --upload --targets simplesub/SimpleSub --upload-port /dev/serial/by-id/usb-ArduPilot_mRoX21_3C001D000C51383437313533-if00,/dev/serial/by-id/usb-AUAV_PX4_BL_AUAV_X2.1_0-if00 
