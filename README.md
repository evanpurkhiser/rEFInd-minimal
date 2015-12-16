## Custom rEFInd-minimal Theme

[rEFInd](http://www.rodsbooks.com/refind/) is a simplistic boot manager for UEFI
based systems. This is a clean and minimal theme for it.

*TODO: Screenshot here*

### Usage

 1. Locate your refind EFI directory. This is commonly `/boot/EFI/refind`
    though it will depend on where you mount your ESP and where rEFInd is
    installed. `fdisk -l` and `mount` may help.

 2. Clone this repository into your refind configuration directory.

 3. To enable the theme add `include rEFInd-minimal/theme.conf` at the end of
    `refind.conf`.

Your boot entries should be auto-detected. Be careful to remove old Linux kernels and comment out all the example menu entries in `refind.conf`.

### Background sizes

If you find the background does not fit your monitor or is too large you have
three options:

 1. Configure the `banner_scale` option with `fillscreen`. Be aware that this
    may cause some level of quality loss due to resampling! If things look
    fuzzy this may not be the right approch.

 2. Download and resize the [original high-quality wallpaper][wallpaper] and
    replace the `background.png`. Different sizes of the wallpaper are available for download.

 3. Adjust the resolution option in `refind.conf`. Mine is set to `resolution 1920 1080`. Going above
    1920x1080 may have undesirable effects.

You can swap out the background with any other background you like. All you have to do is download it, make sure it is an appropiate size, and for the sake of safety and quality, make sure it is a PNG. Take care to ensure that all the icons are still visible. After you have done this, simply delete the original `background.png` amd replace it with your own `background.png`.

### Attribution

The original [rEFInd-minimal][theme] theme is by [Evan Purkhiser][evan].

The OS icons are from [Lightness for burg][icons] by [SWOriginal][icon-author].

The background is one I found called [Crystals][wallpaper] by [Puscifer91][bg-author] on deviantART.

[theme]: https://github.com/EvanPurkhiser/rEFInd-minimal
[evan]: https://github.com/EvanPurkhiser

[icons]: http://sworiginal.deviantart.com/art/Lightness-for-burg-181461810
[icon-author]: http://sworiginal.deviantart.com/

[wallpaper]: http://puscifer91.deviantart.com/art/Crystals-Wallpaper-4K-504839163
[bg-author]: http://puscifer91.deviantart.com/
