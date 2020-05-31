![wpfind](pics/logo.png)

WPFind
======

The purpose of this script is to find wallpapers among pictures files in directory and sub-directories and move/copy them to a separate directory.
It can be useful when you are trying to clean your mess on your computer ;-)

Requirements
------------

* Ubuntu, Linux Mint (should work on other Ubuntu derivatives)
* detox
* imagemagick

Installation
------------

For Ubuntu 16.04, Linux Mint 18.x, and other derivatives

```
curl -L https://packagecloud.io/makoto/stable/gpgkey | sudo apt-key add -
echo "deb https://packagecloud.io/makoto/stable/ubuntu/ xenial main" | sudo tee /etc/apt/sources.list.d/makoto.list
sudo apt-get update
sudo apt-get install wpfind
```

For Ubuntu 18.04, Linux Mint 19.x, and other derivatives

```
curl -L https://packagecloud.io/makoto/stable/gpgkey | sudo apt-key add -
echo "deb https://packagecloud.io/makoto/stable/ubuntu/ bionic main" | sudo tee /etc/apt/sources.list.d/makoto.list
sudo apt-get update
sudo apt-get install wpfind
```

For Ubuntu 20.04, Linux Mint 20.x, and other derivatives

```
curl -L https://packagecloud.io/makoto/stable/gpgkey | sudo apt-key add -
echo "deb https://packagecloud.io/makoto/stable/ubuntu/ focal main" | sudo tee /etc/apt/sources.list.d/makoto.list
sudo apt-get update
sudo apt-get install wpfind
```

For Arch Linux and other derivatives

```
trizen -S wpfind
```

Usage options
-------------

```
██╗    ██╗██████╗ ███████╗██╗███╗   ██╗██████╗
██║    ██║██╔══██╗██╔════╝██║████╗  ██║██╔══██╗
██║ █╗ ██║██████╔╝█████╗  ██║██╔██╗ ██║██║  ██║
██║███╗██║██╔═══╝ ██╔══╝  ██║██║╚██╗██║██║  ██║
╚███╔███╔╝██║     ██║     ██║██║ ╚████║██████╔╝
 ╚══╝╚══╝ ╚═╝     ╚═╝     ╚═╝╚═╝  ╚═══╝╚═════╝

Find wallpapers recursively in a dir and sub-directories...

Version : 0.1.3
Author : Francois B (Makoto)
Licence : GPLv3

Usage : wpfind [options]
  -c : copy wallpapers found in a specific folder
  -m : move wallpapers found in a specific folder
  -s : interactive mode (ask confirmation before overwriting a file)
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

* Email : francois@makotonoblog.be
* Website : https://makotonoblog.be/wpfind/

Licence
-------

The script is licensed under the terms of the GPLv3