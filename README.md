Papaya
======

A pure JavaScript medical research image viewer.  Current list of features:
- Requires no browser plugin.  Runs in desktop and mobile browsers (iPhone and iPad supported).
- Orthogonal viewer controlled with mouse and keyboard controls.
- Reads NIFTI (.nii and .nii.gz) files.
- Supports overlays and atlas labels.  (Includes sample image and atlas.)
- Supported browsers (min version): Firefox (7), Chrome (7), Safari (6), MobileSafari (iOS 6), IE (10).
- Demo: http://ric.uthscsa.edu/mango/papaya/

![ScreenShot](https://raw.github.com/rii-mango/Papaya/master/README-img.png)

Installation
------
Development: Run `debug.html` with your favorite JavaScript debugger.

Production: Run `build.sh` to create the build files.  For example `build.sh -sample -atlas`.  Include the `-local` flag if 
not intending to store files on a web server.  See the [Papaya Builder](https://github.com/rii-mango/Papaya-Builder) project for more 
information.

```shell
usage: papaya-builder [options]
  -atlas <file>   add atlas
  -help           print this message
  -local          build for local usage
  -root <dir>     papaya project directory
  -sample         include sample image
```

Usage
------
Basic usage:
```html
<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml" lang="en">
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
        <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no"/>
        <meta name="apple-mobile-web-app-capable" content="yes">
        <link rel="stylesheet" type="text/css" href="papaya.css" />
        <script type="text/javascript" src="papaya.js"></script>
        <title>Papaya Viewer</title>
    </head>

    <body>
        <div id="papayaContainer">
            <div id="papayaToolbar"></div>
            <div id="papayaViewer" class="checkForJS"></div>
            <div id="papayaDisplay"></div>
        </div>
    </body>
</html>
```

To automatically load an image by URL:
```html
<div id="papayaViewer" data-load-url="http://www.mysite.com/myimages/myimage.nii.gz"></div>
```
