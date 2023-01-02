# BlurLocker
An [i3lock-color](https://github.com/Raymo111/i3lock-color) Wrapper Script That Reads Colors Directly From Xresources!

## Why
Because [i3lock-color](https://github.com/Raymo111/i3lock-color) looks ugly out of the box, and there are like a billion options you need to set if you actually want it to look decent

## Gallery
![Gruvbox](https://i.imgur.com/Klc78j5.png)
![Nordic](https://i.imgur.com/lfUCcnW.png)

## Installation

### Manual Installation
* install [i3lock-color](https://github.com/Raymo111/i3lock-color) (obviously), and [xgetres](https://github.com/tamirzb/xgetres) (both available in the AUR)
* clone this repository:
```bash
git clone https://gitlab.com/SafwanLjd/BlurLocker.git
```
* copy the executable file to whereever you keep your executables (`/usr/local/bin`, `~/.local/bin`, etc.)


### AUR
This script is available in the Arch User Repository, so if you're using an Arch based distro you can install it with your favorite AUR helper (`paru`, `yay`, etc.)
```bash
paru -S blurlocker
```

## Usage
You can just run `blurlocker`, and it will just work!

However, there's an option you might want to use, the `-n` option:
```
blurlocker -n
```
This will allow you to blur the locker window using a compositor that supports blur like [picom-ibhagwan](https://github.com/ibhagwan/picom), this can be useful as it gets rid of the slight delay between running the script and locking the screen.

### [picom-ibhagwan](https://github.com/ibhagwan/picom) Example Configuration File
```
blur-method             = "kawase";
blur-kern               = "3x3box";
blur-strength           = 5;

# this line disables blur on all other programs that aren't the lock screen
blur-background-exclude = [ "class_g != 'i3lock'" ];
```

You can add or change options as you see fit
