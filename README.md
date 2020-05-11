# 64-bit TrueCrypt for macOS

- Compiled for 64-bit and wxWidgets 3.1. Based on https://github.com/neurodroid/TrueCrypt.
- The file extension `.tc` has been associated with TrueCrypt.

Download [the latest release](https://github.com/nomadli/truecrypt-mac/releases/latest).

To build, you need:
```
brew install nasm pkg-config
brew cask install osxfuse
```

You need to replace your wxmac Formula with [this one](Build/Resources/MacOSX/wxmac.rb).
```
EDITOR=subl brew edit wxmac
brew reinstall wxmac
```

Build your TrueCrypt
```
WX_CONFIG=/usr/local/Cellar/wxmac/3.1.2/bin/wx-config make WXSTATIC=1
```

Get wxFormBuilder for macOS here: https://github.com/wxFormBuilder/wxFormBuilder/releases

For the old 32-bit version, see [this branch](https://github.com/nomadli/truecrypt-mac/tree/old) and [this release](https://github.com/nomadli/truecrypt-mac/releases/tag/v3).
