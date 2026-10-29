# Log Begone (26.x port)

> **Unofficial port to Minecraft 26.3 (Fabric).**
> This is a modified version of [Log Begone](https://github.com/AzureDoom/Log-Begone) by **AzureDoom**
> (itself a fork of *Shut Up Console* by Bravarly), ported by **Samouxx** in October 2026.
> The original mod stopped at Minecraft 1.21.1 and its repository is archived.
> Please report problems with this port [here](https://github.com/Samouxx/Log-Begone/issues), not to the original author.
>
> Changes from the original 1.0.3: ported to Minecraft 26.3, Fabric only (the NeoForge build was dropped),
> single Gradle module, no longer requires Fabric API. The commit history of the `port-26.x` branch explains each change.
>
> License: GPL-3.0, like the original ([LICENSE](LICENSE)).

## What it does

Hides annoying lines from the game and server console and log files.

## Configuration

On first launch the mod creates `config/logbegone.json`. Add the text of the lines you want to hide:

```json
{
  "logbegone": {
    "phrases": ["Disconnecting VANILLA connection attempt"],
    "regex": [".*Channels .*"]
  }
}
```

- `phrases`: a line is hidden if it **contains** one of these texts.
- `regex`: a line is hidden if it **fully matches** one of these regular expressions. Game log lines are checked as
  `[logger name]: message`, so surround your expression with `.*` as in the example.

Restart the game after editing the file.
