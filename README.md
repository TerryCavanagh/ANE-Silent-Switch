Since Adobe Air 3.4, you can support the iPhone mute switch without using a native extension - simply set `SoundMixer.audioPlaybackMode = AudioPlaybackMode.AMBIENT`, like so:

``` as3
import flash.media.SoundMixer;
import flash.media.AudioPlaybackMode;

SoundMixer.audioPlaybackMode = AudioPlaybackMode.AMBIENT;
```

# Air Native Extension for iOS Silent Switch (deprecated)

*Please note that we are no longer able to support this project and are not contributing to it.*

This is an [Air native extension](http://www.adobe.com/devnet/air/native-extensions-for-air.html) for the hardware silent switch on the iOS platform.

This extension enables the hardware silent switch on the phone to mute sounds that are played in an Air project. The extension has a single command that mutes all current and future sounds. The setting must be re-applied when your app returns from the background.

### Version

This is version 1.0 of this extension.

### Binary files

The bin folder contains the compiled extension and the default swc, which can be used for local testing if required by your development environment (Flash Builder shouldn't need it, but other IDEs may).

### Building

Requirements - Adobe Air SDK 3.1 or later, XCode IDE

* Add the FlashRuntimeExtensions.h file from the Adobe Air sdk to the ios/SilentSwitchIosExtension folder in the project.
* Create a copy of the build/example.build.config file in the build folder, calling it build.config and change the properties in this file to match your system.
  * A certificate is required by the build script. This may be a self-signed certificate created by Adobe Air.
* Run the ant build script build.xml. This creates the native extension and default swc file inside the bin folder.

### The test project

A simple test project is included for testing the extension. To build this air project

* Run the ant build script test/build.xml. This creates the test ipa inside the test/bin folder.

### Using the extension

#### Make all current and future sounds obey the silent switch setting -

`SilentSwitch.apply()`

### Example code

You can see the feature in action in the source code of the test project.

### Compiling your project

This is an Air 3.1 extension. Specify the path to the iphone SDK when compiling the project, using the functionality built in to your IDE or the platformsdk parameter if building with adt from the command line or a build script.

### Developers

* [Stick Sports](http://www.sticksports.com/)

### Games using this extension

* [Stick Cricket Super Sixes](http://itunes.apple.com/app/stick-cricket-super-sixes/id483135193?ls=1&mt=8)

## License

```
Air Native Extension for iOS Silent Switch
.................................................

Author: Richard Lord
Owner: Stick Sports Ltd.
http://www.sticksports.com

Copyright (c) 2011, Stick Sports Ltd.
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* Neither the name of Stick Sports Ltd. nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
  
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```
