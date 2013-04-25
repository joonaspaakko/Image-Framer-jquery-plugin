![Image Framer](Image-Framer.jpg)

## Image Framer jquery plugin

Image Framer is very simple jQuery plugin that wraps your images inside a frame. _Actually, despite the name, you can frame any element._


_Website is coming soon._ Currently you can find demo html files in the package.

## Freatures

* All of the frames are flexible to pretty much any image size
* Contains 24 frames
* All frames come in 4 different sizes
* 4 different optional inner shadows
* HTML 5 data-attributes can be used to overwrite the plugin options

## Tested browsers

* _Coming soon..._

## Usage instructions

###1.

* [Download the .zip][1].
* Move `imageframer` folder to you website root.

###2.

Add the following to your web page `<head>`.

```HTML
<!-- Make sure that jquery is linked as well -->
<script type="text/javascript" src="jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="imageframer/if.css" />
<script type="text/javascript" src="imageframer/if.js" ></script>
<script type="text/javascript">
    $(function() {

      $('.frame').imageframer();

    });
</script>
```

###3.

Add the `.frame` class to all elements you wish to frame

## Options

* **frameType:** 'wood' `List of frames below`
* **frameSize:** 4 `Numbers from 1 to 4. 1 is the smallest and 4 is the largest`
* **innerShadow:** null `Numbers from 1 to 4. 1 is the smallest / lightest and 4 is the biggest / darkest `
* **disable:** false `Boolean value`
* **callback:** function() {} `Triggered after everything is generated`

Options example

```html
<script type="text/javascript">
    $(function() {

      $('.frame').imageframer({
          frameType: 'wood3',
          callback: function() {
              $(this).addClass('aClass');
          },
          innerShadow: 1
      });

    });
</script>
```

## List of available frames:

* wood-dark
* wood-dark2
* wood-darkgrey
* wood-darkgreen
* wood-darkorange
* wood-darkred
* wood-light
* wood-light2
* wood-light3
* wood-old
* wood-oldlight
* wood-purple
* wood3
* wood4
* wood5
* wood6
* rock
* metallic
* black
* red
* gold
* gold2
* silver
* silver2


## Data-attributes

Example of all data attributes applied to one image ( minus 'disable' and 'callback' ):

```html
<img
    class="frame"
    data-frame-type="black"
    data-frame-size="3"
    data-inner-shadow="1"
    data-custom-class="myClass"
    src="myImg.jpg" alt=""
/>

```

Example of the disable option:


```html
<img class="frame" data-disable="true" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />

```

Callback can only be used as a data-attribute to disable `callback` for certain elements:

```html
<img class="frame" data-callback="false" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />

```

## Known issues

* The frame images will get 1px shift when you zoom the document ( _not at all zoom levels_ ). Automatic tablet zooming causes this as well, but I really don't find it super distracting. If you are concerned with it, in quite a few situations you can get rid of it by using a frame that doesn't have a shadow. Of course you could replace the shadow with css3 shadow...

## Want to make your own frames?

There's photoshop template and script just for that!

You can get it here: [Photoshop Image Framer Export Script](https://github.com/joonaspaakko/Photoshop-Image-Framer-Export-Script)

## Changelog

####v.1.1.
* Remade all the frames _( Just minor changes )_
* Had to change css positioning due to the new frames that are more refined
* Even though it's not included in the package, I made [Photoshop Image Framer Export Script](https://github.com/joonaspaakko/Photoshop-Image-Framer-Export-Script) that will make it super easy to make frames.

## What's to come (maybe)?

* Moar frames!!!
* Maybe a photoshop script that enables re-color multiple frames at once...?
* I need to refine some of the frame files.
 * top-bottom and right-left images are unnecessary wide for some frame types.
 * I pretty much half-assed the way I named the frames. Need to work on that.


[1]: https://github.com/joonaspaakko/Image-Framer-jquery-plugin/archive/master.zip
