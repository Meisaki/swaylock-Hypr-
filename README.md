# Swaylock-Conf by me
Swaylock is a screen locker for the Sway Wayland compositor.{this config Is Tweaked By Me If you have Problem using it just T_ASK }

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Secure Locking:** Provides a secure way to lock your screen.
- **Integration with Sway:** Specifically designed for use with the Sway Wayland compositor.
- **Customizable Appearance:** Supports theming and customization.

## Installation

### From Source

1. Ensure you have the necessary dependencies installed (Swayidle, etc.).
2. Clone the repository: `git clone https://github.com/swaywm/swaylock.git`
3. Navigate to the project directory: `cd swaylock`
4. Build and install: `make && sudo make install`

### From Package Manager

- On Arch Linux, swaylock is available in the official repositories. Install it with:

```
sudo pacman -S swaylock
```
- On Arch Linux, swayidle is program which need for setting idle-time or timout for swaylock its not pre-installed with swaylock. Install it with:
```
sudo pacman -S swayidle
```  
## Usage
Open terminal enter `swaylock` it will open swaylock as your screen will lock (manually) (do not have swayidle input)
```
swaylock
```
Open your hyprland conf write in section where exec command are there mean execute when system starts so you won't need to manually setup again and again (automatic) (swayidle input as timeout ss )
```
exec-once = swayidle -w timeout 100 'swaylock -f'
```
Just replace 100 with your desired time and save it (is it working just observe)
- you can change appearances just by adding command+desired-setting as it only work for that current-command if you want to make permanent just see config section

## Configuration

### Create Config
- (Config) In most case is not there but can be created by using
```
mkdir $HOME/.config/swaylock
```
- Now Create File name 'config'
```
touch $HOME/.config/swaylock/config
```
- It Was Not there so remember you have to tell swaylock  -C config location
```
swaylock -C $HOME/.config/swaylock/config
```
- Now You can edit with any txt editor (nano)
```
nano $HOME/.config/swaylock/config
```
### Tweaking
- Its divided in to 5 main setting (Normal + Verifying + Cleared + Wrong + Capslock)
  - Normal(28)
     - Ring (1-4)
     - Text (5)
1. `line-color=rrggbbaa` here it change color of border of ring
2. `line-uses-inside=rrggbbaa` here it uses the line color as inside of ring and line (do not use sometime its cause like passsword wrong and  this can be accomplished by just line-color)
3. `line-uses-ring=rrggbbaa` here it uses the opposite of 2 as it use ring color
4. `ring-color=rrggbbaa` here it change color of ring when its idle or typing
5. `font=_____` here you can change font of text
6. `font-size=19` you can set size of font as text but sometime it only change time size not its down
7. `layout-bg-color=rrggbbaa`
8. `
      
     
