# baldi engine

![isabelle](art/picture.png)
new engine that i made for baldi's basics in funkin', and maybe other mods from me or my friends

it does the job + has extensible code, however no mods folder since its what caused issues with my older engines.

## TODO LIST:

- [x] Sorted assets
- [x] Sorted source
- [x] Get rid of base game stuff in source
- [x] Turn Conductor into a flixel plugin (updates independently of MusicBeatState)
- [x] Make source work with new assets
    - [x] Implement FunkinCache
    - [x] Fix BitmapFrontEnd
    - [x] Source assets
    - [x] Implement GPU textures (and maybe reimplement cne's assetslibrarytree???)
- [x] New chart system
    - [x] Create chart system
    - [x] Make it read charts from **Psych / Base Game**
        - [x] Parse metadata
        - [x] Parse notes
        - [x] Parse events
    - [x] Make it read charts from **Codename**
- [x] Complete PlayState rewrite
    - [x] Rewrite controls
    - [x] New chart parser
    - [x] New stage system based on FlxGroups
    - [x] Change Character into an interface (and extend it)
        - [x] Sparrow characters support
        - [x] Animate Atlas characters support
    - [x] New Note system
    - [x] Add sustains to the note system
    - [x] Add score, misses & accuracy
    - [x] Add healthbar & icons
    - [x] Add Game Over screen
    - [x] Make the songs actually finishable
    - [x] Pause Menu
    - [x] Scroll speeds
    - [x] Cutscenes
    - [x] End Cutscene
    - [x] Modchart class with callbacks & stuff
    - [x] Beginning countdown (3 2 1 go)
    - [x] Make combo ratings show up
- [x] Save & Options
    - [ ] Remove Highscore, etc... and replace it by FunkinSave (like CNE)
    - [ ] Add Options
        - [x] Add options saving
        - [ ] Add options menu (??? maybe at the end right before release)
- [ ] Discord RPC
- [ ] Baldi Funkin
- [ ] Menus
    - [ ] Update Freeplay to use icons & config.json
    - [ ] Update Story Menu to a better format

## TODONT LIST:

- [x] "mods" folder

## ADDED FEATURE LIST

- **Reorganized assets**: Got rid of data, images, sounds, etc... Redone for ease of use.
- **Reorganized source**: Now disposed into folders.
- **Rewritten Conductor**: now works as a plugin, allows for any game song to use BPM changes via additional .bpm file (including main menu and gameover)
    - `FlxG.sound.playMusic()` now obsolete, use `Conductor.instance.loadAndPlay()`
- **Rewritten Characters**: Characters now have separate classes and can extend anything that extends FlxSprite (FlxSpriteGroup, FlxAnimate...)
- **Rewritten Stages**: Stages are now FlxGroups separated into singular classes. Since theyre groups, they can be easily interchanged midsong with some coding.
- **Rewritten Chart System**: Charts allows now for more than 2 strumlines (no chart format tho, use the Codename Engine one if you want best compatibility)

## CREDITS
- Yoshman29 - programmer
- Ne_Eo - additional help & added some fixes
- Baldi's Basics in Funkin' team - lol theyre the reason this engine exists
- Funkin Crew - The original game
- mystman12 - for making baldis basics