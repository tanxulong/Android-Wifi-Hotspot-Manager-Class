Android Wifi Hotspot Manager <a href="https://travis-ci.org/nickrussler/Android-Wifi-Hotspot-Manager-Class"><img align="right" src="https://travis-ci.org/nickrussler/Android-Wifi-Hotspot-Manager-Class.svg?branch=master"></a>
==================

A minimalistic Android library (and demo app) which provides access to the private android hotspot API.

With this you can check the current status of the hotspot, enable/disable it, get/set the current AP configuration and also get the list of currently connected clients.

This repository contains a demo project including a widget to control the access point.

## Screenshot
<img src="https://www.whitebyte.info/wp-content/uploads/2012/05/Screenshot_20171110-182526.png" alt="" width="360"  class="aligncenter size-full wp-image-1092" />

## Homepage
http://www.whitebyte.info/android/android-wifi-hotspot-manager-class

## Note
To use this library you do not need root, just in case you are wondering why some methods may not work.
This is due to the fact that most of the internal Android API called within this library is private API and may be deprecated/changed by now.

## License
This project is open source and free, it is available under the [Apache v2 License](http://www.apache.org/licenses/LICENSE-2.0.html).

#comment
From Lollipop till Nougat (21 <= API <= 25)
The hotspot is managed using Reflection APIs as the corresponding methods are hidden and not generally available for 3rd Party applications.

Above Oreo
Android has come up with a new API called LocalOnlyHotspot

https://developer.android.com/reference/android/net/wifi/WifiManager.LocalOnlyHotspotCallback
https://developer.android.com/reference/android/net/wifi/WifiManager.LocalOnlyHotspotReservation
These APIs let us to manage the hotspot if the hotspot is enabled by this app.
