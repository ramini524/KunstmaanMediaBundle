KunstmaanMediaBundle
====================

While building websites for clients we have learned that almost every website benefits from a centralised management of multimedia assets. To facilitate our building process we have created this bundle to add this functionality with the least amount of hassle. Additionally, we want our websites to leverage external services as much as possible, so all video and presentation content is offloaded (manually) to external website.

This bundle provides this centralised module for multimedia assets, and has built in providers for local images, [YouTube](http://www.youtube.com), [Vimeo](http://www.vimeo.com) and [Dailymotion](http://www.Dailymotion.com) video's, [Speakerdeck](http://speakerdeck.com/) and [Slideshare](http://www.slideshare.net/) presentations, and generic local files.

No central asset management module is useful without some pretty advanced image editing functionality. To provide this we have integrated the [Aviary](http://www.aviary.com/) image editing service right from the interface. This provides us with all the tools needed to manage images in a website, without the need of a Photoshop or other image editing tool on the administrators computer.

View some screenshots on this bundles [github page](http://kunstmaan.github.com/KunstmaanMediaBundle).

> ** Important Note **
>
> Once again, we're not reinventing code here, the code in this bundle is heavily inspired from the [AnoMediaBundle](https://github.com/benjamindulau/AnoMediaBundle) 
> which on his turn is based on the [SonataMediaBundle](https://github.com/sonata-project/SonataMediaBundle).
>
> The KunstmaanMediaBundle is different in the way that it's base handles galleries, videos and slides without the hassle of adding them yourself.
>
> We didn't chose to fork the AnoMediaBundle but started the KunstmaanMediaBundle from scratch. This way we could find out the inner workings of the AnoMediaBundle more easily. 
> But keep in mind the code in the AnoMediaBundle is reused at a lot of places.

Licensing
---------

The KunstmaanMediaBundle is licensed under the MIT License.

    The MIT License (MIT)
    Copyright (c) 2012 Kunstmaan NV
    
    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated 
    documentation files (the "Software"), to deal in the Software without restriction, including without limitation 
    the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, 
    and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all copies or substantial portions 
    of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED 
    TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL 
    THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF 
    CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS 
    IN THE SOFTWARE.


Installation requirements
-------------------------

The KunstmaanMediaBundle depends on the hard work of the PHP and Symfony community and uses the following bundles. Please refer to their documentation for installation and configuration instructions. 

* [Imagine](https://github.com/avalanche123/Imagine)
* [AvalancheImagineBundle](https://github.com/avalanche123/AvalancheImagineBundle)
* [Gaufrette](https://github.com/KnpLabs/Gaufrette)

Installation instructions
-------------------------
Installation is straightforward, add the following lines to your deps file and running vendors install.

```
[KunstmaanMediaBundle]
    git=https://github.com/Kunstmaan/KunstmaanMediaBundle.git
    target=/bundles/Kunstmaan/MediaBundle
```

Register the Kunstmaan namespace in your autoload.php file:

```
'Kunstmaan'        => __DIR__.'/../vendor/bundles'
```

Add the KunstmaanMediaBundle to your AppKernel.php file:

```
new Kunstmaan\MediaBundle\KunstmaanMediaBundle(),
```

Known issues
------------

This is the first public alpha release of this bundle. Sensible unit tests are still missing, and the coupling with our other bundles is still too tight. Expect these issues to be solved by version v0.2

Continuous testing on Travis CI is implemented: [![Build Status](https://secure.travis-ci.org/Kunstmaan/KunstmaanMediaBundle.png?branch=master)](http://travis-ci.org/Kunstmaan/KunstmaanMediaBundle)

Reporting an issue or a feature request
---------------------------------------

Issues and feature requests are tracked in the [Github issue tracker](https://github.com/Kunstmaan/KunstmaanMediaBundle/issues).

When reporting a bug, it may be a good idea to reproduce it in a basic project built using the Symfony Standard Edition to allow developers of the bundle to reproduce the issue by simply cloning it and following some steps.
