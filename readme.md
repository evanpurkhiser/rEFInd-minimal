## Minimalistic rEFInd theme

[rEFInd](http://www.rodsbooks.com/refind/) is a simplistic boot manager for UEFI
based systems. This is a clean and minimal theme for it.

![rEFInd Minimalistic](http://i.imgur.com/Q26vQJx.jpg)

### Usage

To use this theme you'll want to clone it into the same directory as your rEFInd
efi executable (usually `/boot/EFI/refind/`). Then you will want to add the line
`include minimal-theme/theme.conf` to the end of your `refind.conf`.

To set the icons for your entries you will want to add the `icon` configuration
to each menuentry which points to the icon under `minimal-theme/icons` that you
would like to use for that entry.

Here's an example configuration (from the screenshot)

````
menuentry "Arch Linux" {
	icon /EFI/refind/minimal-theme/icons/grey_arch.png
	loader vmlinuz-linux
	initrd initramfs-linux.img
	options "ro root=UUID=dfb2919d-ff78-48db-a8a7-23f7542c343a loglevel=3"
}

menuentry "Windows" {
	icon /EFI/refind/minimal-theme/icons/grey_windows.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}

menuentry "OSX" {
	icon /EFI/refind/minimal-theme/icons/grey_osx.png
	loader /EFI/Apple/Boot/bootmgfw.efi
}
````

### Attribution

The OS icons are from [Lightness for burg](http://sworiginal.deviantart.com/art/Lightness-for-burg-181461810)
by [SWOriginal](http://sworiginal.deviantart.com/).

The background image was found on [wallbase.cc](http://wallbase.cc) and doesn't seem to have any attributions.
