![Logo](admin/sonos.png)
ioBroker.sonos
==============

[![NPM version](http://img.shields.io/npm/v/iobroker.sonos.svg)](https://www.npmjs.com/package/iobroker.sonos)
[![Downloads](https://img.shields.io/npm/dm/iobroker.sonos.svg)](https://www.npmjs.com/package/iobroker.sonos)

[![NPM](https://nodei.co/npm/iobroker.sonos.png?downloads=true)](https://nodei.co/npm/iobroker.sonos/)

![Screenshot](img/preview1.png)

![Screenshot](img/preview2.png)

Control and monitor SONOS player from ioBroker.

Used packets from Jimmy Shimizu
https://github.com/jishi/node-sonos-discovery and
https://github.com/jishi/node-sonos-web-controller

**This adapter requires node 4.0.0 or higher!**

To allow using sayIt adapter with SONOS, be sure that web adapter is instantiated and running too. Web adapter is required to enable SONOS to read the generated MP3 file from sayIt.

You can use mobile interface too. It can be found under ```http://ipaddress:8083/m/```

TODO: Show queue with covers

## Infos on Grouo handling
* States: coordinator, group_volume, group_muted
* all read/write, to get also changes from Sonos-App
* "coordinator" contains the channel name of the Group-Master (e.g. 192_168_1_99). If Device do not belong to any group the value is eaqual to the own channel name


## Changelog
### 1.6.0 (2017-04-09)
- (justr1) Enhance group Handling

### 1.5.0 (2017-02-23)
- (bluefox) use new configuration dialog

### 1.4.4 (2017-01-29)
- (soef) removeFromGroup extended

### 1.4.3 (2017-01-08)
- (bluefox) Allow to use the sonos web via with proxy

### 1.4.2 (2016-12-29)
- (bluefox) add states for vis control and change some roles

### 1.3.1 (2016-12-27)
- (bluefox) Fix TTS if fade was 0

### 1.3.0 (2016-12-13)
- (bluefox) Fix api changes of SONOS module

### 1.2.1 (2016-12-10)
- (bluefox) add web adapter as dependency

### 1.2.0 (2016-10-25)
- (bluefox) tts was rewritten because of new sonos-discovery interface

### 1.1.0 (2016-10-20)
- (bluefox) update sonos npm packets
- (bluefox) configurable fadeIn and fadeOut

### 1.0.0 (2016-10-16)
- (bluefox) fix fade out

### 0.2.2 (2016-09-30)
- (bluefox) fix types of states

### 0.2.1 (2016-09-25)
- (soef) fixed restore of radio after sayIt

### 0.2.0 (2016-07-28)
- (soef) fixed restore of radio after sayIt
- (bluefox) fix log outputs
- (bluefox) update libraries and use fix versions of it

### 0.1.10 (2016-05-26)
- (bluefox) check type of "state"

### 0.1.9 (2016-05-20)
- (bluefox) change default port to 8080

### 0.1.8 (2016-02-22)
- (hagen) - Better handling of radio stations (show -> album, streamInfo -> artist)
- (hagen) New state 'current_type' to tell if a track or radio is playing
- (hagen) (Hopefully) fixed the unreliable cover art update

### 0.1.7 (2015-09-14)
- (bluefox) fix favorites set

### 0.1.6 (2015-02-25)
- (bluefox) implement tts if radio is playing

### 0.1.5 (2015-02-13)
- (bluefox) set volume by TTS

### 0.1.4 (2015-01-04)
- (bluefox) catch errors if states deleted

### 0.1.3 (2015-01-02)
- (bluefox) enable npm install

### 0.1.2 (2014-12-12)
- (bluefox) redirect logging messages to ioBroker

### 0.1.1 (2014-12-04)
- (bluefox) translate grid in config dialog

### 0.1.0 (2014-12-04)
- (bluefox) use sonos-web-controller module as tarball from git

### 0.0.5 (2014-11-24)
- (bluefox) support of new naming concept


### 0.0.4 (2014-11-22)
- (bluefox) support of text to speech

### 0.0.3 (2014-11-01)
- (bluefox) support of text to speech and cover image

### 0.0.2 (2014-11-01)
- (bluefox) improve configuration edit

## Configuration
- Web server - [optional] If web server enabled or not
- Port       - If Webserver is enabled, so the port for this. Default 8083
- Update of elapsed time(ms) - Interval in ms how often to update elapsed timer when the title is playing. (Default 2000)

## License

The MIT License (MIT)

Copyright (c) 2014-2016, bluefox <dogafox@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
