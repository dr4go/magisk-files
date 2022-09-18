# Magisk Delta

This repo hosts Magisk delta related files

![](https://github.com/topjohnwu/Magisk/raw/master/docs/images/logo.png)

## Introduction

#### **This is not an officially supported [topjohnwu](https://github.com/topjohnwu) project**. 

> If you are looking for official Magisk source, you are in the wrong place, please [go to this page and download Official Magisk](https://github.com/topjohnwu/Magisk)

A custom Magisk by dr4go (with different pkg name), which is always synchronized with HuskyDG's Magisk.

## Download

> If you are fine with official Magisk setup, it is recommended to stay. If you choose to use Magisk Delta, make sure you read all FAQs and changelog before using Magisk Delta.

### Stable / Beta

> For most user, Stable build is recommended.

#### Stable

- [Magisk 25.2-delta](https://huskydg.github.io/download/magisk/25.2-delta.apk)
- [Source code](https://huskydg.github.io/download/magisk/25.2-delta.zip)
- [Changelog](https://github.com/HuskyDG/magisk-files/blob/main/note_stable.md)

#### Beta

> Currently same as Stable channel


### Canary / Debug

⚠ Only accept bugreports from Magisk Delta variant.

#### Download

- [Download Canary](https://dr4go.github.io/magisk-files/f4e7881e/app-release.apk)
- [Download Debug](https://dr4go.github.io/magisk-files/f4e7881e/app-debug.apk)

#### Source code

- [Changelog](https://github.com/dr4go/magisk-files/f4e7881e/note.md)
- [Source code](https://github.com/topjohnwu/Magisk/tree/f4e7881e)

## FAQ

### Is Zygisk DenyList an alternate feature of MagiskHide?

No. Although Denylist could look a bit like MagiskHide but it cannot be considered as an alternate solution of MagiskHide. Denylist is the feature to prevent modules from loading in applications that are on the denylist thus break some modules. Apps are on Denylist can still know Zygisk if it wants to. It doesn't even hide the presence of zygisk. In additional, Zygisk itself has many problems and leaves traces that cannot be hidden.

### Is MagiskHide dead?

- Depend on what you expected. MagiskHide is still effective to hide root from apps.

- MagiskHide does not require to inject into zygote or depend on Zygisk, so it can void being detectable, does not like other hiding injection modules. And hiding root is not necessary to inject into zygote.

- Since Magisk Delta 25203, MagiskHide has switched to rely on logcat to avoid Tracer detection.

- On Android 11+, it is unnecessary to inject into zygote in order to handle isolated process or app zygote.

- MagiskHide is removed from official Magisk. Leave users no choice to hide root from apps.

- Zygisk is easily detected and has some problems that cannot be hidden.

- Riru has RiruHide to hide itself from maps. There are no such feature exists on zygisk. And Riru does not working if zygisk is enabled.

### How to switch from current Magisk to Magisk Delta and vice versa?

> Some Mediatek devices prevent boot partition from being modified (or kernel doesn't allow to modify boot image) after booting. When directly installing, you might end up with "/dev/xxxx is read-only" error or the installation seems to be successful but actually fails. In this case, please try patching boot image with Magisk app and flash it from Custom Recovery or Fastboot instead. 

The fast way to migrate to Magisk Delta or switch back to official Magisk: Just flash magisk app like a module.

1. Rename the extension `magisk.apk` to `magisk.zip`
2. Open Magisk app, click "Modules" tab -> "Install from storage" and choose `magisk.zip`
3. Reboot your device


### How to install Magisk into emulator (such as NoxPlayer, LDPlayer, etc...)?

> Currently, only Magisk Delta support Magisk installation into system partition. Although emulator has ramdisk image, patching ramdisk is not used because ramdisk is stored in seperate partition with very SMALL disk size that is not enough to store Magisk binaries.

1. Enable Root access in emulator settings
2. Install and open Magisk Delta
3. Grant root access to Magisk Delta, click "Install" under Magisk field and use "Direct Install into system partition" option instead of "Direct Install" option. If you don't see this option, close and re-open Magisk Delta app.
4. Disable Root access in emulator settings

### Why not restore Magisk modules online repo?

The official Magisk modules repository is dead and no longer maintained. Due to that, add them back is meanless. However, [Fox2Code](https://github.com/Fox2Code) has developed [Magisk Modules Manager](https://github.com/Fox2Code/FoxMagiskModuleManager)  app which allows you to download Magisk modules online.

## Donate me

- Paypal: [paypal.me/huskydg](http://paypal.me/huskydg)
- You can now donate me if you want. Remember, I will not make this as a monetization tool and donate is not obligated. Thanks for all your supports and hope you have a good day! 👍


## Other links

- [Internal Documents](./docs/internal-guide.md)

## Other stuff

- [Riru Core](https://github.com/RikkaApps/Riru/releases)
- [Isolated MagiskHider](https://github.com/HuskyDG/riru-momohider/releases)

## License

Our license obviously is the same as [Magisk's license](https://github.com/topjohnwu/Magisk#License)

```
Magisk, including all git submodules are free software:
you can redistribute it and/or modify it under the terms of the
GNU General Public License as published by the Free Software Foundation,
either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
