# RTCM2MavLink

This project was written to take raw serial RTCM streams from a
SparkFun RTK Express kit and send it along to a PixHawk wrapped in
MavLink packets.  This gets rid of the need to use Mission Planner
RTK/Inject screen or other ground station to pass along your RTCM
packets from your base station.

## To Do

Only handle GPS RTCM packets.  Filter out other messages.  Current
code is going to try to stuff everything into MavLink and that will
be bad if there is stuff that shouldn't be there.

Handle only 4 f ragmented packets on MavLink.  Dump them if they wont
fit.

Optionally enable wifi and connect to NTRIP server to pull RTCM
packets.  Replaces need for ground station in the middle.

## Photos

Two cables coming out of the ESP32.  One for the RTCM coming in from
the Sparkfun Kit.  And the other going to the LoraSerial transmitter.

<img src="./assets/PXL_20241028_232930614.jpg" alt="drawing" width="480"/>

The ESP32 I chose to use since it really only needs two serial ports.

<img src="./assets/PXL_20241028_232939784.jpg" alt="drawing" width="480"/>

The GPS antenna mounted for my base.  I know the mountain is blocking
some of the back but thats all I could do.  Seems to work great anyhow.

<img src="./assets/PXL_20241010_163851877.jpg" alt="drawing" width="480"/>

The car with the beta ESP32 and rough wiring to make sure everything
worked in the code.  Have since removed the ESP32 and placed it in the
same cabinet as the base is transmitting from.  Only the LoraSerial remains.

<img src="./assets/PXL_20241025_202051220.jpg" alt="drawing" width="480"/>

My Traxxas F-150 High Edition truck with a purple cube and a Hero4 GPS.
Works amazing!

<img src="./assets/PXL_20241025_215801971.jpg" alt="drawing" width="480"/>
