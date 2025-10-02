See [WYVRN Documentation](https://doc.wyvrn.com/) for the latest info.

# WYVRN SDK in Unreal Engine (Built-in)

The WYVRN SDK is part of the Unreal Engine which can be used to control `Chroma` and haptics.

For the latest setup instructions see the `WYVRN` [Epic MegaJam 2025 Documentation](https://doc.wyvrn.com/docs/wyvrn-sdk/epic-megajam-2025/).

The pre-released installer for the [WYVRN SDK Runtime](https://github.com/WyvrnOfficial/UnrealEngine/releases/tag/wyvrn_sdk_runtime) can be found in `Github Releases`.

## Getting Started

**To get started open Unreal Engine.**

![image_1](images/image_1.png)

**Create a new project or open an existing project. Both `Blueprints` and `C++` are supported.**

![image_2](images/image_2.png)

**Use the `Edit` menu and select the `Plugins` menu item.**

![image_3](images/image_3.png)

**Search `chroma` to select the `Razer Chroma Devices` plugin.**

![image_4](images/image_4.png)

**Activate the plugin and click `Yes` to accept the experimental plugin.**
![image_5](images/image_5.png)

**Click `Restart Now` to relaunch the Unreal Engine with the plugin enabled.**

![image_6](images/image_6.png)

**The plugin is now enabled.**

![image_7](images/image_7.png)

**Use the `Edit` menu and select the `Project Settings` menu item.**

![image_8](images/image_8.png)

**Scroll down to the `Plugins` section and select the `Razer Chroma Settings` project settings.**

![image_9](images/image_9.png)

**Check `Create Razer Chroma Input Device` and expand `App Info` to update the details for `Application Title`, `Application Description`, `Author Name`, and `Author Contact`**

![image_10](images/image_10.png)

 **The `App Info` specifies details that appear in the `CHROMA APPS` list.**

 ![image_11](images/image_11.png)

**Open the level blueprint.**

![image_12](images/image_12.png)

**Create a `Set Event Name` node which is used to trigger Chroma and haptics events by name.**

![image_13](images/image_13.png)

**Name any of your game events and pass the name to `Set Event Name`.**

![image_14](images/image_14.png)

This causes the external command to fire.

```shell
Demo_Development_Editor: play NameAnyGameEvent
```

**Save the level to save the blueprint changes.**
![image_15](images/image_15.png)

**`Chroma` and haptics events can be controlled via the [WYVRN Configuration](https://doc.wyvrn.com/docs/wyvrn-sdk/wyvrn-configuration/) and the game can create a custom configuration that is used from `C:\Program Files (x86)\InterHaptics\HapticFolders\Title_Configuration`.**

The [WYVRN Effect Library](https://chroma.razer.com/WyvrnEffectsLibrary/) provides a set of existing event names to choose from.

![image_17](images/image_17.png)

**Use [SynesthesiaServer.exe](https://github.com/WyvrnOfficial/RazerSensa_DevKit/tree/master/Apps/Synesthesia/ReleaseConsole) from the WyvrnOfficial Github repository to verify event names are being sent properly by the game events.**

The public repository can be downloaded or cloned to get access to the tools.

```shell
git clone https://github.com/WyvrnOfficial/RazerSensa_DevKit
```

Use `Apps/Synesthesia/ReleaseConsole/SynesthesiaServer.exe` in order to view game events sent by `SetEventName`.

![image_16](images/image_16.png)
