![myInstallScript](https://sirenacorp.be/wp-content/uploads/2016/01/logo-1.png)

WPFind
======

The purpose of this script is to find wallpapers among pictures files in directory and sub-directories and move/copy them to a separate directory.
It can be useful when you are trying to clean your mess on your computer ;-)

Requirements
------------

* Ubuntu, Linux Mint (should work on other Ubuntu derivatives)
* detox
```
sudo apt-get install detox
```
* imagemagick
```
sudo apt-get install imagemagick
```

Installation
------------

```
sudo dpkg -i wpfind.deb
```
If requirements are not installed, the previous command will fail because the dependencies are not satisfied.

Fix it by (should install detox and/or imagemagick if they are missing)
```
sudo apt-get install -f
```

Usage options
-------------

```
 _       ______  _______           __
| |     / / __ \/ ____(_)___  ____/ /
| | /| / / /_/ / /_  / / __ \/ __  /
| |/ |/ / ____/ __/ / / / / / /_/ /  
|__/|__/_/   /_/   /_/_/ /_/\__,_/   

Find wallpapers recursively in the current dir and sub-directories...

Version : 0.1
Author : Francois B (Makoto)
Licence : GPLv3

Usage : wpfind [options]
  -c : copy wallpapers found in a specific folder
  -m : move wallpapers found in a specific folder
  -i <directory_to_analyze_to_find_wallpapers>  (default: current directory)
  -o <wallpapers_found_save_directory>  (default: wpfiles inside the current directory)
  -w <minimum_pixel_width>  (default: 1920px)
  -v : verbose mode
  -h : show help & informations
```

Usage examples
--------------

Copy wallpapers in the current directory and sub-directories with minimum width of 1920px to wpfiles

```
wpfind -c
```

Move wallpapers in the current directory and sub-directories with minimum width of 1920px to wpfiles

```
wpfind -m
```

Move wallpapers in the /home/user/MyPics directory and sub-directories with minimum width of 2560px to /home/user/MyWP directory

```
wpfind -m -w 2560 -i /home/user/MyPics -o /home/user/MyWP
```

Credits
-------

This script has been written by Francois B. (Makotosan/Shakasan)

* Email : shakasan@sirenacorp.be
* Website : https://sirenacorp.be/

Licence
-------

The script is licensed under the terms of the GPLv3

Changelog
---------
2017-09-02 : initial release 0.1
