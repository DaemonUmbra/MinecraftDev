<p align="center"><a href="https://minecraftdev.org/"><img src="https://minecraftdev.org/assets/icon.svg" height="120"></img></a></p>

Minecraft Development for IntelliJ
==================================

|    Build     | Status |
|--------------|--------|
| **TeamCity** |[![TeamCity Build Status](https://tc.demonwav.com/app/rest/builds/buildType:(id:MinecraftDev_Build)/statusIcon)](https://ci.demonwav.com/viewType.html?buildTypeId=MinecraftDev_Build)|
| **Nightly**  |[![TeamCity Nightly Status](https://tc.demonwav.com/app/rest/builds/buildType:(id:MinecraftDev_Nightly)/statusIcon)](https://ci.demonwav.com/viewType.html?buildTypeId=MinecraftDev_Nightly)|
| **Linux**    |[![Linux GitHub Action Status](https://github.com/minecraft-dev/MinecraftDev/workflows/Linux%20Build/badge.svg?branch=dev&event=push)](https://github.com/minecraft-dev/MinecraftDev/actions?query=workflow%3A%22Linux+Build%22)|
| **macOS**    |[![macOS GitHub Action Status](https://github.com/minecraft-dev/MinecraftDev/workflows/macOS%20Build/badge.svg?branch=dev&event=push)](https://github.com/minecraft-dev/MinecraftDev/actions?query=workflow%3A%22macOS+Build%22)|
| **Windows**  |[![Windows GitHub Action Status](https://github.com/minecraft-dev/MinecraftDev/workflows/Windows%20Build/badge.svg?branch=dev&event=push)](https://github.com/minecraft-dev/MinecraftDev/actions?query=workflow%3A%22Windows+Build%22)|

Info and Documentation [![Current Release](https://img.shields.io/badge/release-2019.3--1.3.4-orange.svg?style=flat-square)](https://plugins.jetbrains.com/plugin/8327)
----------------------

<a href="https://discord.gg/j6UNcfr"><img src="https://i.imgur.com/JXu9C1G.png" height="48px"></img></a>

Visit [https://minecraftdev.org](https://minecraftdev.org) for a little information about the project.


Installation
------------

This plugin is available on the [JetBrains IntelliJ plugin repository](https://plugins.jetbrains.com/plugin/8327).

Because of this, you can install the plugin through IntelliJ's internal plugin browser. Navigate to
`File -> Settings -> Plugins` and click the `Browse Repositories...` button at the bottom of the window. In the search
box, simply search for `Minecraft`. You can install it from there and restart IntelliJ to activate the plugin.

Building
--------

JDK 8 is required.

Build the plugin with:

`./gradlew build`

The output .zip file for the plugin will be in `build/distributions`.

Test the plugin in IntelliJ with:

`./gradlew runIde`

Code is generated during the build task, to run the generation task without building use:

`./gradlew generate`

This task is necessary to work on the code without errors before the initial build.

To format the code in this project:

`./gradlew format`

This will format using `ktlint` described below in the [style guide](#style-guide) section below.

The [Gradle IntelliJ Plugin](https://github.com/JetBrains/gradle-intellij-plugin)
will handle downloading the IntelliJ dependencies and packaging the
plugin.

Style Guide
-----------

This projects follows the opinionated [`ktlint`](https://ktlint.github.io/) linter and formatter. It uses the
[`ktlint-gradle`](https://github.com/jlleitschuh/ktlint-gradle) plugin to automatically check and format the code in
this repo.

IDE Setup
---------

It's recommended to run the `ktlintApplyToIdea` and `addKtlintFormatGitPreCommitHook` tasks to configure your
IDE with `ktlint` style settings and to automatically format this project's code before committing:

```
./gradlew ktlintApplyToIdea addKtlintFormatGitPreCommitHook
```

Developers
----------

- Project Owner - [**@DemonWav** - Kyle Wood](https://github.com/DemonWav)
- [**@Minecrell**](https://github.com/Minecrell)
- [**@PaleoCrafter** - Marvin Rösch](https://github.com/PaleoCrafter)
- [**@RedNesto**](https://github.com/RedNesto)

#### **Significant Contributors**

- [**@gabizou** - Gabriel Harris-Rouquette](https://github.com/gabizou)
- [**@kashike** - Riley Park](https://github.com/kashike)
- [**@jamierocks** - Jamie Mansfield](https://github.com/jamierocks)

License
-------

This project is licensed under [MIT](license.txt).

Supported Platforms
-------------------

- [![Bukkit Icon](src/main/resources/assets/icons/platform/Bukkit.png?raw=true) **Bukkit**](https://hub.spigotmc.org/stash/projects/SPIGOT/repos/bukkit/browse) ([![Spigot Icon](src/main/resources/assets/icons/platform/Spigot.png?raw=true) Spigot](https://spigotmc.org/) and [![Paper Icon](src/main/resources/assets/icons/platform/Paper.png?raw=true) Paper](https://papermc.io/))
- [![Sponge Icon](src/main/resources/assets/icons/platform/Sponge_dark.png?raw=true) **Sponge**](https://www.spongepowered.org/)
- [![Forge Icon](src/main/resources/assets/icons/platform/Forge.png?raw=true) **Minecraft Forge**](http://minecraftforge.net/forum)
- [![LiteLoader Icon](src/main/resources/assets/icons/platform/LiteLoader.png?raw=true) **LiteLoader**](http://www.liteloader.com/)
- [![MCP Icon](src/main/resources/assets/icons/platform/MCP.png?raw=true) **MCP**](http://www.modcoderpack.com/)
- [![Mixins Icon](src/main/resources/assets/icons/platform/Mixins_dark.png?raw=true) **Mixins**](https://github.com/SpongePowered/Mixin)
- [![BungeeCord Icon](src/main/resources/assets/icons/platform/BungeeCord.png?raw=true) **BungeeCord**](https://www.spigotmc.org/wiki/bungeecord/) ([![Waterfall Icon](src/main/resources/assets/icons/platform/Waterfall.png?raw=true) Waterfall](https://github.com/WaterfallMC))
