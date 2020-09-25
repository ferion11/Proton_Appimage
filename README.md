[![Build Status](https://travis-ci.com/ferion11/Proton_Appimage.svg?branch=master)](https://travis-ci.com/ferion11/Proton_Appimage) [![AppImage Build](https://img.shields.io/badge/AppImage-build-blue)](https://github.com/ferion11/Proton_Appimage/releases)

# Appimage For Wine Proton

>  Appimage for last Wine Proton 32bits from PlayOnLinux. You can just download the Appimage, put in the directory you like and make symbolic links for it (for wine, wineserver...).

####  1- Download proton-VERSION.AppImage for your AppImage directory [here][PROTON_release_continuous]. And if you want the normal wine, you can get it [here_link][WINE_normal]
####  2- Make executable:
```
$ chmod +x proton-VERSION.AppImage
```
####  3- Make the wine link in your bin directory:
```
$ ln -s proton-VERSION.AppImage wine
```
####  4- Make the wineserver link (for winetricks) in your bin directory:
```
$ ln -s proton-VERSION.AppImage wineserver
```

##  Have set:
- WINEARCH=win32 (fixed and can't be changed)
- WINEPREFIX=~/.proton32 (can be changed if needed)

##  Usage:
####  For configuration, just run "wine" (it will run the winecfg) or:
```
$ wine winecfg
```
####  For regedit:
```
wine regedit
```
####  For your Apps:
```
wine xyz.exe
```
####  If you use PRIME, you can use something like that too:
```
DRI_PRIME=1 wine xyz.exe
```
####  Optional 1- To test the OpenGL of your video card:
```
$ wine glxinfo32
$ wine glxgears32 -info
$ wine shape32
```
####  Optional 2- You can use PRIME too:
```
$ DRI_PRIME=1 wine glxgears32 -info
```
####  Optional 3- Configure and run vulkan (only intel and radeon are supported now):
- Configure for intel:
```
$ wine f11conf vulkan intel
```
-  Configure for radeon:
```
$ wine f11conf vulkan radeon
```
-  Configure for intel and radeon together:
```
$ wine f11conf vulkan radeon:intel
```
-  Test vulkan:
```
$ wine vulkaninfo32
$ wine vkcube32
```

[PROTON_release_continuous]: https://github.com/ferion11/Proton_Appimage/releases/tag/continuous "here"
[WINE_normal]: https://github.com/ferion11/Wine_Appimage "here_link"
 