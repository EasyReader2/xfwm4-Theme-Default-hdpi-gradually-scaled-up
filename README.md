# xfwm4 Theme Default-hdpi gradually scaled up for modern HDPI Screens

I have gradually scaled up the xfwm4 theme (for the Xfce4 Window Manager) for HDPI screens, based on the script suggested by https://github.com/CouldBeThis/xfwm4-themes-hiDPI :

```
find . -name "*.xpm" -o -name "*.png" | xargs -I {} magick {} -sample "${Scaling}%" {}
```

I have 'improved' the theme by replacing the X button, which always ends up fuzzy and pixilated, by a black square. The main trick was to edit relevant xpm files in a text editor and then fill up the X shape until it becomes a square. I also changed the RGB value for . (dot).

To make the theme also work for dark themes, I used the following command:  
```
sed -i 's/#      c #000000/#      c #808080/g' *.xpm
```

The folders in the .zip file can be directly extracted to ~/.local/share/themes .
You will then be able to pick a suitably scaled window title from inside the Xfce application **Window Manager** to match your chosen scale.
 
