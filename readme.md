# What is this?

This is a development enviroment made for the ESP32. All you need to do is install Vagrant and run:

````
vagrant up
````

# Troubleshooting

### Driver

If you don't see your board you might need to intall an additional driver.
In order to find out what driver you'll need, identify the chip on your board that is responsible
for communicating with your PC, e.g Google search the part names and check if there's a driver for it. My board uses
the CP2102 chip.

If you're or Mac and you installed the driver, make sure that the driver is loaded.
To check run: `kextstat | grep silabs`, to load the driver run: `sudo kextutil /Library/Extensions/SiLabsUSBDriver.kext`.

Issue: [nodemcu-devkit-v1.0/issues/2](https://github.com/nodemcu/nodemcu-devkit-v1.0/issues/2)

### Bad Usb Cable

Make sure that the usb cable you're using can do data transfer. Some cables are used only for charging. 
