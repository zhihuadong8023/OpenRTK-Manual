OpenRTK330LI Reference Application Specification
================================================

1.0 Introduction
----------------

The Aceinna OpenRTK330LI module integrates a commercial
multi-constellation, multi-frequency Global Navigation Satellite System
(**GNSS**) chipset (supports GPS, GALILEO, GLONASS and Beidou), a
triple-redundant 6-axis (3-axis accelerometer and 3-axis gyro) **MEMS**
Inertial Measurement Unit (**IMU**), and a ST M4 MCU as the processor.
OpenRTK330LI module is targeted for commecial applicaiton for the mass
market that requires a reliable, high-precision and yet cost effective
**GNSS/INS** integrated positioning solution.

The following contents layout the features of the module and detailed
specifications for designed **reference applicaitons**.

2.0 Detailed specifications:
----------------------------

Features
~~~~~~~~

-  100 Hz GNSS/INS integrated position, velocity and attitude solution
-  GPS (L1/L2 or L1/L5), GLONASS (L1/L2), GALILEO (E1/E5), Beidou
   (B1I/B2I),QZSS (L1), and SBAS
-  RTK/PPP algorithms on-board for up to centimetre accuracy
-  Triple-redundant IMU (OpenIMU330) for INS positioning solution
-  Open source GNSS/INS integration algorithm code
-  Ethernet, UART, SPI and CAN interfaces

INS reference applications
~~~~~~~~~~~~~~~~~~~~~~~~~~

There are two Apps developed for INS applicaitons: the **Android App**
(mobile) and the **Web App** (non-mobile, e.g. desktop).

App settings
^^^^^^^^^^^^

Android App:

-  OpenRTK330LI acts as NTRIP client connects with NTRIP server via
   Android smartphone (with 4G) Bluetooth connectivity (with Aceinna
   RTKTool App installed) to fetch GNSS RTK/PPP correction data stream
-  Default bluetooth device name "OpenRTK\_0001" shows on Android
   smartphone, which can be changed through installed Aceinna RTKTool
   App
-  Configure NTRIP server settings on Anroid smartphone in the provided
   Aceinna RTKTool App

Web App:

-  Plug in a RJ45 cable from a local network to OpenRTK330LI Ethernet
   port

-  OpenRTK330LI acts as NTRIP client connects with NTRIP server via host
   (e.g. Desktop) to fetch GNSS RTK/PPP correction data stream
-  DHCP IP address is ued as default, if no success, manually setup a
   static IP: ip = 192.168.1.110, netmask = 255.255.255.0, gateway =
   192.168.1.1

Primary data ports:
^^^^^^^^^^^^^^^^^^^

-  Ethnet (RJ45): Web App
-  UART: Android App
-  SPI
-  CAN

Output messages:
^^^^^^^^^^^^^^^^

-  Android App: using UART2 and connected ESP32 Bluetooth module
-  send gpgga to android app via bluetooth
-  Web App:
-  send gpgga to NTRIP server via ethernet
-  OpenIMU330BA/INS UART3 Default Baud Rate: 460.8kb/s
-  OpenIMU330BA/INS UART3 Default Data Output Rate: 100Hz
-  OpenIMU330BA/INS UART3 Default Message: pos packet('NV'), snr
   packet('SA') and skyview packet('SK').

Input Messages:
^^^^^^^^^^^^^^^

-  Android App:
-  Web App:

Debug/Console Port:
^^^^^^^^^^^^^^^^^^^

-  OpenIMU330BA/INS UART1 Default Baud Rate: 460.8kb/s

   -  Default debug data output

Performance (Drive Test):
^^^^^^^^^^^^^^^^^^^^^^^^^

3.0 Test Requirements:
----------------------

4.0 Test Results:
-----------------

-  List results from Tests required in 3.0
-  List release notes Summary
-  Link to Downloadable/Install Ready Binaries on Aceinna Developer Site

