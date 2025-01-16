# MacOSXoptims
Optimisations to speed up animatons for Mac OS, version early 2025.
- no guarantees given :D

In default settings, Mac OS has animations that are verry slow and often hinder productivity. Here are alle the terminal commands to speed up your Mac's animations.

## general Settings
Settings>Accessibility>Display --> "Reduce motion"  

## General animation speed
```
defaults write com.apple.finder DisableAllAnimations -bool true 
``` 

## Finder Animations

Disables all Finder animations. Relaunch Finder afterwards via Command-Option-Escape.  
Two commands one for show / hide: 
```
defaults write com.apple.dock springboard-show-duration -float .1

defaults write com.apple.dock springboard-hide-duration -float .1 
```

## Launchpad Animations

Speeds up the Launchpad show/hide animation:
```
defaults write com.apple.dock springboard-page-duration -float .2 
```

## Dock hide/show animation
Here are two options to change the behavior of the Dock when it is slow to appear.  

delete the animation:  
```
defaults write com.apple.dock autohide-time-modifier -int 0; killall Dock 
```

reduce the animation to minimum:  
```
defaults write com.apple.dock autohide-time-modifier -float .1; killall Dock
```

## Switch Desktops / Spaces animaton



# REVERSE Modifications

You can reverse all modifications by replacing the defaults write command with defaults delete and omitting the value after the key. E.g. 
```
defaults delete com.apple.finder DisableAllAnimations
```
