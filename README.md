# Luna

A Beat Saber mod that allows you to easily interact with the game using Lua.

# Getting Started
To get started, create a new project using the [Luna Script Template](https://github.com/MillzyDev/Luna-Script-Template).
Once that is done, pay your attention to the `main.lua` file. This file is the main "entrypoint" for your mod script.

#### ⚠️ SECUIRTY ⚠️
> For security reasons the Lua standard library is not available within Luna addons. This is to prevent malware from being embedded in addons.

## Addon Metadata
Installed addons must have a table labelled metadata that contains information about your mod. It is already in your `main.lua` file, if you used the template.

You should be able to see the metadata table at the top of your `main.lua` file, if you used the template.

Make sure that this exists and all of the fields are present. The addon will not load if the metadata is invalid.

```lua
ADDON_METADATA = {
    _lunaVersion="1.0.0", -- Luna version the addon was designed to run with
    name="#{name}", -- The name of the addon
    author="#{author}", -- The author of the addon (thats you!)
    version="#{version}" -- The version of the addon
}
```

The variable **MUST** have the signature `ADDON_METADATA` otherwise it will not work.

## Entrypoint Functions
Entrypoint functions are where Luna will invoke your code.

If you used the template, you will see that an example entrypoint is already present.

```lua
-- declare entrypoints here
function onApp()
    luna.log("My Luna addon loads!");
end
```

`onApp` is the entrypoint used here, but there are many others. All entrypoints are listed below.

- `onApp()`
- `onMenu()`
- `onStandardPlayer()`
- `onCampaignPlayer()`
- `onMultiplayer()`
- `onPlayer()` - invoked on `onStandardPlayer()`, `onCampaignPlayer()` and `onMultiplayer()`.
- `onTutorial()`
- `onGameCore()`
- `onMultiplayerCore()`
- `onSingleplayer()` - invoked on `onStandardPlayer()`, `onCampaignPlayer()` and `onTutorial()`.
- `onConnectedPlayer()`
- `onAlwaysMultiplayer()`
- `onInactiveMultiplayer()`

## Credits

* [zoller27osu](https://github.com/zoller27osu), [Sc2ad](https://github.com/Sc2ad) and [jakibaki](https://github.com/jakibaki) - [beatsaber-hook](https://github.com/sc2ad/beatsaber-hook)
* [raftario](https://github.com/raftario)
* [Lauriethefish](https://github.com/Lauriethefish), [danrouse](https://github.com/danrouse) and [Bobby Shmurner](https://github.com/BobbyShmurner) for [this template](https://github.com/Lauriethefish/quest-mod-template)
