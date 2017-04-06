# Wallpaper

This is a Debian Package with more than 350 wallpapers and a script to change the wallpaper according to a defined time. 
The default time is 60 seconds. It is not a debian binary, but it is ready for packaging... If you have any other distro that doesn't support deb packages you should just clone the repository and move the folders from here to the root folder.

# Debian way
clone the repository with the command:
```
git clone https://github.com/mauricioph/wallpaper.git
```
Give the right permission to the post install file and the gwallpaper
``` 
sudo chmod 0555 wallpaper/DEBIAN/postinst wallpaper/usr/local/bin/gwallpaper 

```
Build the package
```
dpkg-deb --build wallpaper
```

Install the package
```
dpkg --install wallpaper.deb
```
or 
```
gdebi-gtk wallpaper.deb
```
To call the script type gwallpaper. If there is any permission problems the script is located at /usr/local/bin/gwallpaper

# Other distros way
If your distro does not support deb package follow this instructions.

clone the repository with the command:
```
git clone https://github.com/mauricioph/wallpaper.git
```
go to the repository folder
```
cd wallpaper/
```
copy all the files in the usr folder to the root folder
```
sudo mv usr/ /
```
call the script by typing 
gwallpaper
