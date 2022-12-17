# Patcher for Dwarf Fortress.exe of steam version of DF

How to use: just unpack df-steam-translate-hook.zip to the game's directory and run df-steam-hook-launcher.exe file. It will run the game with translation applied.

For your language you'll need to prepare csv file from the [hardcoded_steam.po resource on transifex](https://www.transifex.com/dwarf-fortress-translation/dwarf-fortress-steam/hardcoded_steam/). The package contains csv file for Esperanto encoded into latin3 encoding.

To do this, you need to use tools from [df-gettext-toolkit](https://github.com/dfint/df-gettext-toolkit) repository, see the first example in "Usage examples". The last parameter must be an encoding which is relevant for your language. E.g. for Esperanto I used latin3.

Also you'll probably need to modify `curses_640x300.png` font in the `data/art` directory of the game according to the encoding you've chosen on the to encode csv file. You don't need to redraw the entire font just add characters which is necessary to display text in your language correctly.

Later I'll add posibility to create csv file using [df-translation-client](https://github.com/dfint/df-translation-client).

Some useful key combinations for translators:

1. <kbd>CTRL</kbd>+<kbd>F1</kbd> - activates autoupdate of text in the game when csv file is modified;
2. <kbd>CTRL</kbd>+<kbd>F2</kbd>  - deactivates the previous option;
3. <kbd>CTRL</kbd>+<kbd>F3</kbd>  - switches the translation off;
3. <kbd>CTRL</kbd>+<kbd>F4</kbd> - switches the translation on and updates the translation from the csv file.

When you press any of these combinations, you'll have a message box with a message saing that the action is completed successfully.

Sometimes the message appears on the background behind the game window, so you need to find it and press OK in it.
