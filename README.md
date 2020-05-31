# Hackintosh Catalina (10.5.5) Guide for Gigabyte Z390 Aorus Master (OpenCore) with FileVault

This build is "Vanilla". I used [this guide](https://dortania.github.io/OpenCore-Desktop-Guide/) as a starting point, with references and checking to [CMER's awesome guide](https://github.com/cmer/gigabyte-z390-aorus-master-hackintosh/blob/master/README.md).

The biggest difference is that I have FileVault and the GUI OS picker enabled, and I've updated the kexts, SSDTs, etc to the latest for 0.5.8 and 10.15.5

Yes - this is totally ripped from CMER - all credit to him.

### Hardware

See my [Hardware List](https://pcpartpicker.com/list/4LYjk6) on PCPartsPicker.

![About This Mac](images/AboutThisMac.png)

### What's Working/What's Not

##### Working
- Ethernet
- Onboard Audio (including digital audio)
- APFS
- Sleep/Wake
- All USB ports at 3.x speed
- iMessage
- App Store
- Facetime
- APFS
- Handoff
- Bluetooth & Wi-Fi (via Broadcom adapter - I ordered this from eBay: Dual Band BCM94360CS2 PCI-E 867Mbps 802.11AC BT4.0 Wifi PCI-Express Adapter Card)
- Unlock with Apple Watch
- Airdrop
- AirPlay
- Continuity
- ALL DRMs:
  - iTunes Movies (FairPlay 1.x)
  - Netflix (FairPlay 2.x/3.x)
  - Some Amazon Prime content, but not all. (FairPlay 2.x/3.x)
  - Apple TV+ (FairPlay 4.x)
- Power Nap
- NVRAM
- FileVault


##### Not Working (as expected)
- Built-in WIFI - disabled in BIOS - I use Ethernet for primary networking, and the keep the Broadcom card for wifi purely so Airdrop, unlock with AppleWatch etc work.
- Onboard Bluetooth - I use the Broadcom card.


### Step By Step Instructions

I just followed the [OpenCore Desktop Guide](https://dortania.github.io/OpenCore-Desktop-Guide/). When in doubt, just look at my KEXTs, drivers and config.list for guidance.


### USB Port Map & SSDT

See [CMER's USB_MAP.md](https://github.com/cmer/gigabyte-z390-aorus-master-hackintosh/blob/master/USB_MAP.md) for a map of all the ports on the Aorus Z390 Master.


### My EFI

You are welcome to use my EFI folder. However, make sure you set the following:

- SystemSerialNumber
- SystemUUID
- MLB
