# XFCE-day-and-night-theme
You can switch themes and wallpapers from a terminal in XFCE.



```
[Name of command] ()  {
xfce-theme-manager --theme=[Themes] --wmborder=[Window Borders] --controls=[Controls]
xfce-theme-manager --icons=[Icons]
xfconf-query -c xfce4-desktop -p /backdrop/screen0/[Monitor]/workspace0/last-image -s
}

[Name of command] () {
xfce-theme-manager --theme=[Themes] --wmborder=[Window Borders] --controls=[Controls]
xfce-theme-manager --icons=[Icons]
xfconf-query -c xfce4-desktop -p /backdrop/screen0/[Monitor]/workspace0/last-image -s
}
```


1. You will need to install Xfce-Theme-Manager from
https://github.com/KeithDHedger/Xfce-Theme-Manager

2. Use the xfconf-query to set wallpapers.

3. With Xfce-Theme-Manager you can change several things. Please read
README https://github.com/KeithDHedger/Xfce-Theme-Manager/blob/master/README

4. Use
xfconf-query -c xfce4-desktop -l | grep "last-image$"
to find out what is your monitor.

5. Then use
xfconf-query -c xfce4-desktop -p /backdrop/screen0/[Monitor]/workspace0/last-image -s PATH_OF_NEW_IMAGE
to change wallpaper.

6. Put this in your .bashrc
