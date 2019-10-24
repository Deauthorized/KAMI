#### This is now a continuation of zeroeightysix's KAMI. Please make an issue there if your bug does not happen here, and vice versa. 
#### Note that zeroeightysix's may not receive frequent updates anymore.

#### please use the release, the current build ~~edited~~ it does not work, gradle mcp srg source went down

# KAMI

[![Build Status](https://travis-ci.com/S-B99/KAMI.svg?branch=master)](https://travis-ci.com/S-B99/KAMI)
[![Issues](https://img.shields.io/github/issues/S-B99/kami.svg)](https://github.com/S-B99/kami/issues)
[![Discord Mine](https://img.shields.io/discord/573954110454366214?label=chat%20on%20mine&logo=discord&logoColor=white)](https://discord.gg/KfpqwZB)

[![Build Status](https://travis-ci.com/zeroeightysix/KAMI.svg?branch=master)](https://travis-ci.com/zeroeightysix/KAMI)
[![Issues Master](https://img.shields.io/github/issues/zeroeightysix/KAMI?label=issues%20086)](https://github.com/zeroeightysix/kami/issues)
[![Discord Master](https://img.shields.io/discord/496724196542513174?label=chat%20on%20086&logo=discord&logoColor=white)](https://discord.gg/9hvwgeg)

A Minecraft utility mod for anarchy servers.

See [forgehax](https://github.com/fr1kin/forgehax) for a more polished equivalent. Some features in KAMI may be based on those of forgehax, as it was sometimes used it as reference. Forgehax may also be missing some KAMI features. Client compatibility between these two should be fine, but please mention that you're using other clients if you do have an issue.

Please note Baritone is no longer included. Download the standalone jar [from here](https://github.com/cabaletta/baritone/releases).

This is by no means a finished project, nor is it a "cheat" or "hack" for anything, it is a *utility* mod.

## Status


[Everything here is planned for sure.](https://github.com/zeroeightysix/KAMI/pull/114), [along with here](https://github.com/S-B99/KAMI/issues/12)

This is currently in slowed development. Maintainance and further development is planned in the next couple months.

## Preview

<details>
 <summary>Click to view images</summary>

 ![GUI](.github/IMAGES/gui.png)
 
 ![CrystalAura](.github/IMAGES/crystalAura.png)

</details>

# How do I

##### Open the GUI
Press Y.

##### Use commands
The default prefix is `.`. Commands are used through chat, use `.commands` for a list of commands.

##### Bind modules
Run `.bind <module> <key>`.

Right Shift is `shift` and Left Arrow is `left` for example, while letters are just `y`.

##### Change command prefix
By using the command `prefix <prefix>` without the `<>`(by default, `. <newprefix>`) or after having ran KAMI (make sure it's closed), editing your configuration file (find it using `config path` in-game) and changing the value of `commandPrefix` to change the prefix.

##### Change Custom Chat ending
Edit line 19 in `kami/src/main/java/me/zeroeightysix/kami/module/modules/misc/CustomChat.java`
Change the `\u23D0` characters to something else you want, [use this website to do it](https://www.branah.com/unicode-converter).
Paste text in the first box and copy the output from the second.

This will be implemented with a command in the near future, see issue #11

## Troubleshooting

Please reference the main [troubleshooting page](docs/TROUBLESHOOTING.md)

If you have an issue or problem and it's not listed there, please [open a new issue](../../issues/new/choose) and a contributor will help you further.

## Installing

KAMI is a forge mod. Start by downloading the latest version of [1.12.2 forge](https://files.minecraftforge.net/).
1. Install forge
2. Navigate to your `.minecraft` directory.
   * **Linux**: `~/.minecraft`
   * **Windows**: `%appdata%/.minecraft`
3. Navigate to the `mods` directory. If it doesn't exist, create it.
4. Obtain the KAMI `.jar` file.
   * By **downloading** it: see [releases](../../releases)
   * By **building** it: see [building](#building).
5. Place the `.jar` file in your mods directory.

## Building
#### Linux

You can build by running these commands (without the `<>`) in a terminal with the current directory being KAMI. (EG. `cd ~/Downloads/KAMI`)
```
chmod +x gradlew
./gradlew <args>
```

Possible arguments:
```
build
mkdir
rmOld
copy
```
If you use more then one then it must be in that order. 

Build is required, `mkdir` makes the `mods/1.12.2` directory, `rmOld` removes old versions of KAMI\* in that directory, and `copy` copies the build release to the `mods/1.12.2` directory. 

\*`rmOld` removes any jars ending in `-release.jar`, which is the format KAMI uses. If you use any other mod that uses that naming scheme please remove old versions manually.

If you prefer copying it manually, find a file in `build/libs` called `KAMI-<minecraftVersion>-<kamiVersion>-**release**.jar` which you can copy to the `mods/1.12.2` folder of a minecraft instance that has forge installed.

Note: This assumes your minecraft folder is in the default location under your home folder.

<<<<<<< HEAD
Note: Any argument other then `build` assumes you downloaded KAMI to a nested folder inside your home folder. For example `~/Downloads/KAMI` or `~/Documents/KAMI`. This will be fixed as per [issue #15](https://github.com/S-B99/KAMI/issues/15)

=======
>>>>>>> 8c7508f... update readme with disclaimer
#### Windows

You can build by running these commands in a terminal with the current directory being KAMI. (EG. `cd C:\Users\Username\Downloads\KAMI`)
```
gradlew.bat build
```

To copy on windows run `autocopy.bat`

If you prefer copying it manually, find a file in `build/libs` called `KAMI-<minecraftVersion>-<kamiVersion>-**release**.jar` which you can copy to the `mods\1.12.2` folder of a minecraft instance that has forge installed.

<<<<<<< HEAD
Note: This assumes your minecraft folder is in the default location under your home folder.

## TODO

- [ ] fix 3 sprints existing
- [ ] clean up the readme
- [ ] possibly use a wiki?

## Contributing

You are free to clone, modify KAMI and make pull requests as you wish. To set up your development environment, make use of the following commands:

```
git clone https://github.com/S-B99/KAMI/
cd KAMI
```

On GNU/Linux, run `chmod +x gradlew` and for the following commands use `./gradlew` instead of `gradlew.bat`

Of-course you can also use a Gradle installation if you for some reason want another version of gradle

```
gradlew.bat setupDecompWorkspace
```
Import KAMI into your IDE of choice. If you use IntelliJ, import from the `build.gradle` file and run `gradlew.bat genIntellijRuns`

If you do not wish to run from an IDE, use `gradlew.bat runClient` to run KAMI.
=======
Note: This assumes your minecraft folder is in the default location under your %appdata% folder.
>>>>>>> 8c7508f... update readme with disclaimer

## Thank you

[zeroeightysix](https://github.com/zeroeightysix) for the original [KAMI](https://github.com/zeroeightysix/KAMI)

[ZeroMemes](https://github.com/ZeroMemes) for [Alpine](https://github.com/ZeroMemes/Alpine)

[ronmamo](https://github.com/ronmamo/) for [Reflections](https://github.com/ronmamo/reflections)

The [minecraft forge team](https://github.com/MinecraftForge) for [forge](https://files.minecraftforge.net/)
