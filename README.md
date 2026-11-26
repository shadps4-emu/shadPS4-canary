# shadPS4 Canary #16

Built from [main@057999812](https://github.com/shadps4-emu/shadPS4/commit/0579998122d99fbd0cc0f371e096d210be3440bc) with these pull requests:

| Pull Request | Commit | Title | Author | Merged? |
|----|----|----|----|----|
| [#5190](https://github.com/shadps4-emu/shadPS4/pull/5190) | [`ba622f00b`](https://github.com/shadps4-emu/shadPS4/pull/5190/commits/ba622f00bb2c3ff5e69eaaf40ee69f703c09f620) | video_core / renderer_vulkan: PM4 packet improvements and draw predication | [mavethee](https://github.com/mavethee) | Yes |
| [#5548](https://github.com/shadps4-emu/shadPS4/pull/5548) | [`69e831d8b`](https://github.com/shadps4-emu/shadPS4/pull/5548/commits/69e831d8b511d3b6cb23d6b5a3c92296b7cf4685) | cpu_patches: rewrite FS overrides to GS in place on Linux and FreeBSD | [mavethee](https://github.com/mavethee) | Yes |
| [#5582](https://github.com/shadps4-emu/shadPS4/pull/5582) | [`89029beb8`](https://github.com/shadps4-emu/shadPS4/pull/5582/commits/89029beb859607ea8f234b74824a8a514ac12524) | video_core: Implement hardware occlusion queries | [mavethee](https://github.com/mavethee) | No (no changes) |
| [#5670](https://github.com/shadps4-emu/shadPS4/pull/5670) | [`b71389ccd`](https://github.com/shadps4-emu/shadPS4/pull/5670/commits/b71389ccdfa384fa0ae93ad5ee2a9b97860f950a) | kernel: Align pthread structure layout and separate host context | [mavethee](https://github.com/mavethee) | Yes |
| [#5700](https://github.com/shadps4-emu/shadPS4/pull/5700) | [`858563fbc`](https://github.com/shadps4-emu/shadPS4/pull/5700/commits/858563fbc2072c29583e091fb1d089d932a5c062) | kernel: Make sceKernelWaitEventFlag block in an alertable wait | [RikuKH3](https://github.com/RikuKH3) | Yes |
| [#5713](https://github.com/shadps4-emu/shadPS4/pull/5713) | [`1fbc0a6ab`](https://github.com/shadps4-emu/shadPS4/pull/5713/commits/1fbc0a6abb760a1e94110a207bee64b769d46201) | shader_recompiler: DS_ORDERED_COUNT | [baggins183](https://github.com/baggins183) | Yes |
| [#5738](https://github.com/shadps4-emu/shadPS4/pull/5738) | [`baaf6a387`](https://github.com/shadps4-emu/shadPS4/pull/5738/commits/baaf6a38725c3de16cdfb40f77041e1f8d21856d) | shader_recompiler: Support off-chip and DYNAMIC_HS tessellation | [vjt](https://github.com/vjt) | Yes |
| [#5739](https://github.com/shadps4-emu/shadPS4/pull/5739) | [`98505c369`](https://github.com/shadps4-emu/shadPS4/pull/5739/commits/98505c3694c23ed595aee58016d3974844a414d3) | shader_recompiler: Keep image address operands alive with a no-op | [vjt](https://github.com/vjt) | Yes |
| [#5745](https://github.com/shadps4-emu/shadPS4/pull/5745) | [`5edf35d3e`](https://github.com/shadps4-emu/shadPS4/pull/5745/commits/5edf35d3e5436e31e9fd4e3f062ed1c53c2ebc33) | video_core: Unmap texture cache images on the GPU thread | [vjt](https://github.com/vjt) | Yes |
| [#5754](https://github.com/shadps4-emu/shadPS4/pull/5754) | [`2f2c8404c`](https://github.com/shadps4-emu/shadPS4/pull/5754/commits/2f2c8404c17efd5edbdbbcda1e20da635abf2b9e) | video_core: texture binding improvements | [LNDF](https://github.com/LNDF) | Yes |
| [#5768](https://github.com/shadps4-emu/shadPS4/pull/5768) | [`6204747a1`](https://github.com/shadps4-emu/shadPS4/pull/5768/commits/6204747a11cdb65064bc173c118ec0bafd65dda1) | shader_recompiler: Do 32_32 image atomics on an R64ui view | [vjt](https://github.com/vjt) | Yes |
| [#5769](https://github.com/shadps4-emu/shadPS4/pull/5769) | [`f49b78b0d`](https://github.com/shadps4-emu/shadPS4/pull/5769/commits/f49b78b0da7a6c3ae1f66217337622e9c688b077) | shader_recompiler: Handle a T# dword 1 masked with an immediate | [vjt](https://github.com/vjt) | Yes |


End of merge log. The original README.md follows.

-----

<!--
SPDX-FileCopyrightText: 2026 shadPS4 Emulator Project
SPDX-License-Identifier: GPL-2.0-or-later
-->

<h1 align="center">
  <br>
  <a href="https://shadps4.net/"><img src="https://github.com/shadps4-emu/shadPS4/blob/main/.github/shadps4.png" width="220"></a>
  <br>
  <b>shadPS4</b>
  <br>
</h1>

<h1 align="center">
 <a href="https://discord.gg/bFJxfftGW6">
        <img src="https://img.shields.io/discord/1080089157554155590?color=5865F2&label=shadPS4%20Discord&logo=Discord&logoColor=white" width="275">
 <a href="https://github.com/shadps4-emu/shadPS4/releases/latest">
        <img src="https://img.shields.io/github/downloads/shadps4-emu/shadPS4/total.svg" width="140">
 <a href="https://shadps4.net/">
        <img src="https://img.shields.io/badge/shadPS4-website-8A2BE2" width="150">
 <a href="https://x.com/shadps4">
        <img src="https://img.shields.io/badge/-Join%20us-black?logo=X&logoColor=white" width="100">
 <a href="https://github.com/shadps4-emu/shadPS4/stargazers">
        <img src="https://img.shields.io/github/stars/shadps4-emu/shadPS4" width="120">
</h1>

|               Bloodborne by From Software                   |                     Hatsune Miku Project DIVA Future Tone by SEGA                         |
| :-----------------------------------------------------------: | :--------------------------------------------------------------------------------------------: |
| ![Bloodborne screenshot](./documents/Screenshots/1.png) | ![Project DIVA screenshot](./documents/Screenshots/2.png) |

|                  Yakuza 0 by SEGA                     |                 DRIVECLUB™ by Evolution Studios                    |
| :------------------------------------------------------------------------: | :------------------------------------------------------------------: |
| ![Yakuza screenshot](./documents/Screenshots/3.png) | ![DRIVECLUB screenshot](./documents/Screenshots/4.png) |

# General information

**shadPS4** is an early **PlayStation 4** emulator for **Windows**, **Linux** and **macOS** written in C++.

> [!IMPORTANT]
> This is the emulator core, which does not include a GUI. If you just want to use the emulator as an end user, download the [**QtLauncher**](https://github.com/shadps4-emu/shadps4-qtlauncher/releases) instead.

If you encounter problems or have doubts, do not hesitate to look at the [**Quickstart**](https://github.com/shadps4-emu/shadPS4/wiki/I.-Quick-start-%5BUsers%5D).\
To verify that a game works, you can look at [**shadPS4 Game Compatibility**](https://github.com/shadps4-compatibility/shadps4-game-compatibility).\
To discuss shadPS4 development, suggest ideas or to ask for help, join our [**Discord server**](https://discord.gg/bFJxfftGW6).\
To get the latest news, go to our [**X (Twitter)**](https://x.com/shadps4) or our [**website**](https://shadps4.net/).\
You can donate to the project via our [**Kofi page**](https://ko-fi.com/shadps4).

# Status

> [!IMPORTANT]
> shadPS4 is early in development, don't expect a flawless experience.

Currently, the emulator can successfully run games like [**Bloodborne**](https://www.youtube.com/watch?v=5sZgWyVflFM), [**Dark Souls Remastered**](https://www.youtube.com/watch?v=-3PA-Xwszts), [**Red Dead Redemption**](https://www.youtube.com/watch?v=Al7yz_5nLag), and many other games.

# Why

This project began for fun. Given our limited free time, it may take some time before shadPS4 can run more complex games, but we're committed to making small, regular updates.

# Building

## Docker

For building shadPS4 in a containerized environment using Docker and VSCode, check the instructions here:  
[**Docker Build Instructions**](https://github.com/shadps4-emu/shadPS4/blob/main/documents/building-docker.md)

## Windows

Check the build instructions for [**Windows**](https://github.com/shadps4-emu/shadPS4/blob/main/documents/building-windows.md).

## Linux

Check the build instructions for [**Linux**](https://github.com/shadps4-emu/shadPS4/blob/main/documents/building-linux.md).

## macOS

Check the build instructions for [**macOS**](https://github.com/shadps4-emu/shadPS4/blob/main/documents/building-macos.md).

> [!IMPORTANT]
> macOS users need at least macOS 26.0 to run shadPS4. Intel Macs are not supported.

# Usage examples

> [!IMPORTANT]
> For a user-friendly GUI, download the [**QtLauncher**](https://github.com/shadps4-emu/shadps4-qtlauncher/releases).

To get the list of all available commands and also a more detailed description of what each command does, please refer to the `--help` flag's output.

Below is a list of commonly used command patterns:
```sh
shadPS4 CUSA00001 # Searches for a game folder called CUSA00001 in the list of game install folders, and boots it.
shadPS4 --fullscreen true --config-clean CUSA00001    # the game argument is always the last one,
shadPS4 -g CUSA00001 --fullscreen true --config-clean # ...unless manually specified otherwise.
shadPS4 /path/to/game.elf # Boots a PS4 ELF file directly. Useful if you want to boot an executable that is not named eboot.bin.
shadPS4 CUSA00001 -- -flag1 -flag2 # Passes '-flag1' and '-flag2' to the game executable in argv.
```

# Debugging and reporting issues

For more information on how to test, debug and report issues with the emulator or games, read the [**Debugging documentation**](https://github.com/shadps4-emu/shadPS4/blob/main/documents/Debugging/Debugging.md).

# Keyboard and Mouse Mappings

> [!NOTE]
> Some keyboards may also require you to hold the Fn key to use the F\* keys. Mac users should use the Command key instead of Control, and need to use Command+F11 for full screen to avoid conflicting with system key bindings.

| Button | Function |
|-------------|-------------|
F10 | FPS Counter
Ctrl+F10 | Video Debug Info
F11 | Fullscreen
F12 | Trigger RenderDoc Capture (or game-only screenshot if RenderDoc is unavailable)
Alt+F12 | Capture screenshot including HUD/dialog overlays

> [!NOTE]
> Xbox and DualShock controllers work out of the box.

| Controller button | Keyboard equivalent |
|-------------|-------------|
LEFT AXIS UP | W |
LEFT AXIS DOWN | S |
LEFT AXIS LEFT | A |
LEFT AXIS RIGHT | D |
RIGHT AXIS UP | I |
RIGHT AXIS DOWN | K |
RIGHT AXIS LEFT | J |
RIGHT AXIS RIGHT | L |
TRIANGLE | Numpad 8 or C |
CIRCLE | Numpad 6 or B |
CROSS | Numpad 2 or N |
SQUARE | Numpad 4 or V |
PAD UP | UP |
PAD DOWN | DOWN |
PAD LEFT | LEFT |
PAD RIGHT | RIGHT |
OPTIONS | RETURN |
BACK BUTTON / TOUCH PAD | SPACE |
L1 | Q |
R1 | U |
L2 | E |
R2 | O |
L3 | X |
R3 | M |

Keyboard and mouse inputs can be customized in the settings menu by clicking the Controller button, and further details and help on controls are  also found there. Custom bindings are saved per-game. Inputs support up to three keys per binding, mouse buttons, mouse movement mapped to joystick input, and more.


# Firmware files

shadPS4 can load some PlayStation 4 firmware files.
The following firmware modules are supported and must be placed in shadPS4's `sys_modules` folder.

<div align="center">

| Modules                        | Modules                        | Modules                        | Modules                        |
|--------------------------------|--------------------------------|--------------------------------|--------------------------------|
| libSceAt9Enc.sprx              | libSceAudiodec.sprx            | libSceAudiodecCpu.sprx         | libSceAudiodecCpuDdp.sprx      |
| libSceAudiodecCpuDtsHdLbr.sprx | libSceAudiodecCpuHevag.sprx    | libSceAudiodecCpuM4aac.sprx    | libSceAvPlayer.sprx            |
| libSceAvPlayerStreaming.sprx   | libSceBeisobmf.sprx            | libSceBemp2sys.sprx            | libSceCesCs.sprx               |
| libSceFont.sprx                | libSceFontFt.sprx              | libSceFreeTypeOl.sprx          | libSceFreeTypeOptOl.sprx       |
| libSceFreeTypeOt.sprx          | libSceJpegDec.sprx             | libSceJpegEnc.sprx             | libSceJson.sprx                |
| libSceJson2.sprx               | libSceLibcInternal.sprx        | libSceNgs2.sprx                | libScePngEnc.sprx              |
| libScePsmKitSystem.sprx        | libSceRtc.sprx                 | libSceRudp.sprx                | libSceSystemGesture.sprx       |
| libSceUlt.sprx                 | libSceWkFontConfig.sprx        | libSceXml.sprx                 | libSceDepth.sprx               |
| libScePadTracker.sprx          | libSceMoveTracker.sprx         |
</div>

> [!Caution]
> The above modules are required to run the games properly and must be dumped from your legally owned PlayStation 4 console.



# Main team

- [**georgemoralis**](https://github.com/georgemoralis)
- [**psucien**](https://github.com/psucien)
- [**viniciuslrangel**](https://github.com/viniciuslrangel)
- [**roamic**](https://github.com/roamic)
- [**squidbus**](https://github.com/squidbus)
- [**frodo**](https://github.com/baggins183)
- [**Stephen Miller**](https://github.com/StevenMiller123)
- [**kalaposfos13**](https://github.com/kalaposfos13)

Logo is done by [**Xphalnos**](https://github.com/Xphalnos)

<a href="https://github.com/shadps4-emu/shadPS4/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=shadps4-emu/shadPS4&max=24">
</a>

# Contributing

If you want to contribute, please read the [**CONTRIBUTING.md**](https://github.com/shadps4-emu/shadPS4/blob/main/CONTRIBUTING.md) file.\
Open a PR and we'll check it :)


# Special Thanks

A few noteworthy teams/projects who've helped us along the way are:

- [**Panda3DS**](https://github.com/wheremyfoodat/Panda3DS): A multiplatform 3DS emulator from our co-author wheremyfoodat. They have been incredibly helpful in understanding and solving problems that came up from natively executing the x64 code of PS4 binaries

- [**fpPS4**](https://github.com/red-prig/fpPS4): The fpPS4 team has assisted massively with understanding some of the more complex parts of the PS4 operating system and libraries, by helping with reverse engineering work and research.

- **yuzu**: Our shader compiler has been designed with yuzu's Hades compiler as a blueprint. This allowed us to focus on the challenges of emulating a modern AMD GPU while having a high-quality optimizing shader compiler implementation as a base.

- [**felix86**](https://github.com/OFFTKP/felix86): A new x86-64 → RISC-V Linux userspace emulator

- [**emudev.org**](https://emudev.org/): A network of people interested in the documentation, emulation, simulation and re-implementation of hardware near extinction . Belongs to my friend skmp and me (shadow) also a member of it

# License

- [**GPL-2.0 license**](https://github.com/shadps4-emu/shadPS4/blob/main/LICENSE)
