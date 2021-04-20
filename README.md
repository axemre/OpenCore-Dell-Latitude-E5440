# OpenCore Hackintosh - Dell Latitude E5440
This is the OpenCore configuration I have used (thanks to r33int) on my Dell Latitude E5440 to boot Catalina (not yet tested with Big Sur). It's working well, it may have broken features tho. See 
[Dortania's OpenCore guide](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/haswell.html#deviceproperties) for more information. 

#### Disclaimer:
The following repo is just here for reference purposes. This configuration may be outdated, so I suggest you to make your configuration by reading [Dortania's OpenCore guide](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/haswell.html#deviceproperties) and to use mine as a reference. You may have a slightly different model, which has got different components installed, making your own config is always the best choice!

### My Dell's specs:
* CPU: Intel Core i5 4210U
* RAM: 8GB DDR3
* Graphics: Intel HD 4400 (NO dedicated graphics in my model)
* SSD: 512GB

### Working:

* Display: brightness, integrated graphics with acceleration
* WiFi: using itlwm on a AC-7260 card by Intel, kext not added in my EFI folder, you can easily replace the card with an fully working card in macOS.
* USB: All USB 2.0 and 3.0 ports work flawlessly
* Audio: Works with a small issue (see Bugs)
* integrated microphone
* Sleep
* Ethernet
* HDMI output
* Touchpad
* Integrated camera
* Card reader

### Bugs:

* Audio: After booting, headphone jack does not work, this can be fixed by putting the laptop into sleep and waking it up.
* VGA: Will not work, as this is not supported by macOS for Haswell graphics at all
* NVIDIA graphics: Will not work. If you have a model with NVIDIA graphics, add --wegnoegpu or nv_disable=1 to your boot-args under NVRAM (in config.plist)

