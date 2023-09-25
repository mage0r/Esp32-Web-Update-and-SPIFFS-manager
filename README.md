# Esp32-Web-Update-and-SPIFFS-manager
Basic ESP32 SPIFFS and Wifi manager.

This is based on the work at https://myhomethings.eu/en/esp32-web-updater-and-spiffs-manager/

I found this had a few bugs (particularly edit and delete didn't work).  It was also something like 8 files.
I've found and fixed the bugs and compresed it to 4 files that should drop nicely in to other projects.

I've extended the wifi capabilities to include:
- OTA by default.
- Wifi connect as part of the main loop (so your sketch can start without wifi)
- Fail back to Access Point

The Webserver will load any new files you create to them and apply the processor templating.
This is particularly good for adding or editing your own index.html file.

On first run a config.ini file will be created with the default config options for wifi, passwords etc.  You can then edit that easily through the management interface.
I used Strings because I'm lazy.  Sue me.

The /manage page has been updated, it now tells you how much space is free in a slightly cleaner format.
It also includes the RAM and PSRAM usage, the build date of the sketch and the Project/Version tags.
I moved around the fields to what I would describe as more and less used.

This sketch was built on Arduino IDE 2.2.1.
