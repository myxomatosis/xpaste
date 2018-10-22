# xpaste

This is a tool for copying something and then pasting it where you might not be able to use `crontrol +c` or right click.
A prime example is when using spice console or VNC console. You have a console to your server but maybe you don't have an internet connection.
This program will work with anything that you can use your keyboard to type into. It does so by selecting the window and mimiking keyboard button hits.
It can types much faster than a human. Enabling you to using 100+ character root passwords and typing them in at console in just a few seconds.

Use xpaste to paste whatever is in your copy buffer.
Use xpastef to paste the contents of a file.

## To install
```
wget -O ~/bin/xpaste https://github.com/myxomatosis/xpaste/raw/master/xpaste
wget -O ~/bin/xpastef https://github.com/myxomatosis/xpaste/raw/master/xpastef
chmod +x ~/bin/xpaste*
```
## Dependencies

xdotool
xclip

To install dependencies on a Debian distro run:
```
sudo apt install xdotool xclip
```
To install dependencies on a RedHat distro run:
```
sudo yum install xdotool xclip
```

## Using xpaste and xpastef

xpaste doesn't do line breaks and so is not good with multiple line items
xpastef does add line breaks but also adds an extra line at the end

### xpaste
To use xpaste just copy what you want to paste to your copy buffer using `control +c`, or any other way you normally do it, then run xpaste.
It will prompt for the window to paste in. When you click the window it will immediately start pasting the copy buffer. It does not press the enter key
in order to avoid accidentally entering passwords or other sensitive data to the wrong window.

### xpastef
To use xpastef just run `xpastef` or `xpastef somefile.txt`, then select the window where you want to paste the file.  When you click the window it will immediately start
pasting the selected file to the selected window. It copies line by line hitting enter at the end of each line including the last line. If you run xpastef without
including a file to paste it will prompt you to enter the filename at run time.

## Examples

### xpaste
```
example@example ~ $ xpaste
Select window to paste copy buffer
Paste Complete
example@example ~ $ 
```

### xpastef
```
example@example ~ $ xpastef
What file would you like to paste from [paste.txt]
somefile.txt
Select window to paste somefile.txt
Paste Complete
example@example ~ $
```
```
example@example ~ $ xpastef
What file would you like to paste from [paste.txt]

Select window to paste paste.txt
Paste Complete
example@example ~ $
```
```
example@example ~ $ xpastef file.txt
Select window to paste file.txt
Paste Complete
example@example ~ $
```
