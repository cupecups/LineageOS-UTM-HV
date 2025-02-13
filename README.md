# LINEAGEOS 22.1 UTM/QEMU ARM
## this project image maintener by 0xCAFEBABE as lineageOS builder

![alt text](https://github.com/cupecups/LineageOS-UTM-HV/blob/e060cfb31ff9aece3ce350fa1a0b5e847fd9f6ee/img/about%20Ln.png)
![](https://github.com/cupecups/LineageOS-UTM-HV/blob/655e910cc706b994df101a96ac36815746fedad0/img/showcase.gif)
<br>
i just try to install this OS using UTM HV mode on iphone 14 pm 16.3.1 with hypervisor work on this ios version
# Devices that are able to run this:
- Any Apple silicon Mac
- Any Intel Mac
- iPhone 14 Pro/ 14 Pro Max running iOS 16.0-16.3.1
- Any M1 or M2 iPad running iPadOS 14.5-16.3.1
Any other device will likely never be able to run it.
If you don't own one of these then please stop trying right here

# HOW TO?
# create vm with, at least 2GB RAM, 
1. first virtio disk = 13GB
2. second virtio disk = at least 2GB
3. enable UEFI boot
4. use AC97 sound card
5. use virtio pci gpu
6. insert the installer image as usb drive
7. boot it
8. perform android's factory reset
9. flash the android OTA zip
10. done

# NOTES
Running android on it then would probably be rather funny

You're a bit limited on ram but most things should just work fine 

One issue we still have; which is why this isn't widespread yet;;
There's an issue with the graphics on mobile.
- Using software rendering works but the color space is shifted towards green/red
- Using ANGLE (OpenGL) rendering works but there's a memory leak and as a result the vm will crash within a minute each time 
- Using ANGLE (Metal) causes an issue with something in the renderer and just has no display output
- 3D accelerator/GPU supoorted cause utm crash, that's the known issues which we have no solution yet...

# SCREENSHOOT

![alt text](https://github.com/cupecups/LineageOS-UTM-HV/blob/3c80c0625adc42fd255aa8b86954a99d630e081d/img/ss.png)
<br>

# link
Wiki [LineageOS wiki](https://wiki.lineageos.org/libvirt-qemu#install-lineageos-to-the-virtual-machine)<br/>
Grab UTM apps [UTMapp](https://getutm.app/)
