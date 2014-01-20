==============================================================================
Readme - Software for the PNEV512R EXPLORE-NFC
==============================================================================

1. Document purpose

This document describes the content of the source package as well as known
problems and restrictions.
A separate User Manual describes the first steps how to use the software in
combination with the Hardware.

2. Known problems and restrictions

* Restrictions
The Software is restricted to the Hardware.
The API is intended for the NXP contactless/contact reader ICs, 
as such the API is not to be ported to any technology from any other vendor.
The Software is running on the Raspberry Pi of the Raspberry Pi Foundation. 
NXP will not support porting to any other vendor platform. 

The Software stack as well as the PNEV512R were validated according to CE.


* Known Problems

  - none
	
3. Content

RaspberryPi-EXPLORE-NFC-Startguide.pdf (User manual for the project)

EULA.pdf (EULA - End User License Agreement)

Readme.txt (this document)

card_polling.zip content:

card_polling
+---build
+---source
    +---NxpRdLib_PublicRelease
        +---comps
        +---docs
        +---intfs
        +---types
    +---CMakeLists.txt
    +---main.c
    +---Readme.txt

4. Mandatory material, not included

* Raspberry Pi

5. Building the project

To build the project do the following steps:

1) Change into the folder build.
2) Run the command "cmake ../source".
3) Run the command "make".

6. Revision History

V1.0:
* First packaged version.