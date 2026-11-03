This is a quick vibe-coded fix to the Stellaris Heirs to the Khan bug where the Horde empire randomly becomes hostile to you. Run at your own risk. I pinky swear there is nothing malicious in here, but it could very well break your savegame.

The bug seems to be triggered by any hostile actions between you and the Khan. I am inclined to assumed this is user error, e.g. accidentally telling your fleet to attack a Horde station. Regardless, once in this state there is no way out: you cannot make peace with the Horde because there are no meaningful diplomacy options, and the game is pretty thoroughly broken.

This mod attempts to fix the issue by:

1. Preventing any hostilities between you and the Horde. This is a basic measure which clearly should be the case in the base game.

2. Repeatedly resetting the Horde to be non-hostile. This fixes an already-broken game, and acts as a backup if there is more to the issue than I have diagnosed.

## Installation

Instructions assume Linux and a Flatpak Steam install and a bunch of other things. Making it work on your machine is left as an exercise to the reader.

```bash
   MOD_TAR=~/downloads/heirs_host_fix.tar.gz
   STELLARIS_DIR=~/.var/app/com.valvesoftware.Steam/.local/share/"Paradox Interactive"/Stellaris
   cp -a "${STELLARIS_DIR}/save games" ~/tmp/stellaris-saves-backup-$(date +%F)
   mkdir -p "${STELLARIS_DIR}/mod" && tar xzf "${MOD_TAR}" -C "${STELLARIS_DIR}/mod"
```
