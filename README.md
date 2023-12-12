# Swaylock-Conf by me
Swaylock is a screen locker for the Sway Wayland compositor.{this config Is Tweaked By Me If you have Problem using it just T_ASK }

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)
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
- Its divided in to 5 main setting (Normal + Verifying + Wrong + Cleared + Capslock)
  - Normal(32)
     - Ring (1-4)
     - Text & layout (5-10)
     - Indicator & Basic (11-32)
1. `line-color=rrggbbaa` here it change color of border of ring
2. `line-uses-inside=rrggbbaa` here it uses the line color as inside of ring and line (do not use sometime its cause like password wrong and  this can be accomplished by just line-color)
3. `line-uses-ring` here it uses the opposite of 2 as it use ring color (just add it will apply no need for a parameter or value)
4. `ring-color=rrggbbaa` here it change color of ring when its idle or typing
5. `font=_____` here you can change font of text
6. `font-size=19` you can set size of font as text but sometime it only change time size not its down
7. `layout-bg-color=rrggbbaa` you can change color of box where text is there (in my case it background of box)
8. `layout-border-color=rrggbbaa` its kind of 1 but as its not related to ring
9. `layout-text-color=rrggbbaa` you can set here color of layout text 
10. `text-color=rrggbbaa` as its say it change text color
11. `no-unlock-indicator` it disable the indicator (indicator or box will be there but its removed as visibility) (no value needed)
12. `indicator-idle-visible` use when you want to show always indicator or box in lockscreen (no value) 
13. `indicator-radius=____` radius increase as its value decrease or vice versa
14. `indicator-thickness=___` it will increase ring thickness or radius thickness or vice versa (default value is 10)
15.  `indicator-x-position=___` its used when you want to change indicator or box width (i measured as putting it with random values)
16.  `indicator-y-position=___` its used when you want to change indicator or box height (i measured as putting it with random values)
17.  `inside-color=rrggbbaa` it change color of a indicator
18.  `separator-color=rrggbbaa` it will change color of start and end of segment (segment appear when you type)
19.  `key-hl-color=rrggbbaa`it highlight color of key that segments color (do not get confuse with 17 read it )
20.  `show-keyboard-layout` it will show current layout of keyboard in typing (no value)
21.  `hide-keyboard-layout` it will hide current or others layout in typing (if you set this it will not show even if you show keyboard option) (no value)
22.  `bs-hl-colo` this change color when you press backspace (segment will change color specifically for backspace)
23.  `color=rrggbbaa` change color of the lockscreen (default is white as ffffff)
24.  `image=/path/to/you` add image as lockscreen (replace /path/to/you with your location of image)
25.  `scaling=__` you scale image to fill,stretch,fit,center,tile(if its set into solid_color then even if set image it will show color)
26.  `tiling` its same as if you put scaling as tiling (no value)
27.  `debug` as its say it will output error or (reason sometime)
28.  `ignore-empty-password` it will not react if there is nothing (simple)
29.  `show-failed-attempts` it will print the wrong or invalid attempt (its only print not set value as maximum attempt)
30.  `daemonize` it will removed from terminal after locking (i am not writing this Note: this is the default behavior of i3lock.)
31.  `help` it will show typical help list
32.  `version` it will print version of swaylock  

     - Verfying (4)
       
- `inside-ver-color=rrggbbaa` change color of inside when verifying (pass or string are verifying)
- `line-ver-color=rrggbbaa` change color between ring and line when verifying 
- `ring-ver-color=rrggbbaa` change color of the ring when verifying 
- `text-ver-color` change color of the text when verfying 

     - Wrong(4)
       
- `inside-wrong-color=rrggbbaa` change color of inside when wrong (when input is wrong)
- `line-wrong-color=rrggbbaa` change color between ring and line when wrong
- `ring-wrong-color` change color of the ring when wrong 
- `text-wrong-color` change color of the text when wrong
  
     -  Cleared(4)
       
- `inside-clear-color=rrggbbaa` change color of inside when cleared (it can be appear if use backspace to clear wrong pass or strings)
- `line-clear-color=rrggbbaa` change color between ring and line when cleared
- `ring-clear-color=rrggbbaa` change color of the ring when cleared
- `text-clear-color=rrggbbaa` change color of the text when cleared
  
     -  Capslock(8)
       
- `disable-caps-lock-text` its disable text if capslock is on
- `indicator-caps-lock` its show capslock is on (no value)
- `caps-lock-bs-hl-color=rrggbbaa` its change color of backspace segment of ring if capslock is on
- `caps-lock-key-hl-color=rrggbbaa` its change color of typing segments of ring if capslock is on
- `inside-caps-lock-color=rrggbbaa` its chnage color of inside if capslock is on
- `line-caps-lock-color=rrggbbaa` its chnage color between ring and line if capslock is on
- `ring-caps-lock-color=rrggbbaa` its change color of ring if capslock is on
- `text-caps-lock-color=rrggbbaa` its change color of text if capslock is on

 ## Troubleshooting

- Use debug output to know most problem reason or orgin

- You can use ChatGpt to know more about value  (guess something you knew)

## License

- Refer to `LICENSE` file 
