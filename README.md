# unlocker
lock/unlock ScreenSaver by touching Felica compatible card or device.  
This software depend on libpafe and libusb, please make sure those are already installed.  
  
  
## Supported(Provided) Drivers
* cinnamon(cinnamon-screensaver)
  
Currently, I provide only one driver for cinnamon(cinnamon-screensaver), but you can add a driver for other environment by developping the driver.   
  
## Requirements
* libpafe
* libusb
* dmd
* dub
  
  
## Installation
```zsh
$ git clone https://github.com/alphaKAI/unlocker
$ cd unlocker
$ dub build
```
  
  
## Configuration
Plase make `config.json` at `~/.config/unlocker` and configure it like:  
(`<-` means description, but it is not granted expression in JSON, don't write that in your config.json).  

```json
{
  "driver":"cinnamon", <- driver name
  "interval":5,        <- seconds
  "authorized_keys": {
    "Suica" : {
      "IDm" : "1234567890abc",
      "PMm" : "1234567890"
    },
    "Edy" : {
      "IDm" : "1234567890abc",
      "PMm" : "1234567890"
    }
  }
}
```

  
Note: You can obtain the IDm and PMm of your card with felica\_dump\_util(It locates on subdirectory of this repository).  
  

## License
Copyright (C) 2017 Akihiro Shoji  
This software is released under the MIT licese.  
Please see `LICENSE` for details.  
