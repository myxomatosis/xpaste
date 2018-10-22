# xpaste

This is a tool for copying something and then pasting it where you might not be able to use `crontrol +c` or right click.
A prime example is when using spice console or VNC console. You have a console to your server but maybe you don't have an internet connection.
This program will work with anything that you can use your keyboard to type into. It does so by selecting the window and mimiking keyboard button hits.
It can types much faster than a human. Enabling you to using 100+ character root passwords and typing them in at console in just a few seconds.

Use xpaste to paste whatever is in your copy buffer.
Use xpastef to paste the contents of a file.

## Dependencies

xdotool
xclip

To install dependencies on a Debian distro run:
sudo apt install xdotool xclip

To install dependencies on a RedHat distro run:

sudo yum install xdotool xclip
