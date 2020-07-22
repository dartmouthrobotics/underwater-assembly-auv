# underwater-assembly-auv
Repository containing parts list and CAD files to retrofit a BlueROV2 for improved autonomous operation. The starting point would be a BlueROV2 heavy.

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
