---
title: External Libraries
description: NexT User Docs – Third-party Service Integration – External Libraries
---

### PJAX

[Pjax](https://github.com/MoOx/pjax) is a standalone JavaScript module that uses AJAX (XmlHttpRequest) and `pushState()` to deliver a fast browsing experience.

It allows you to completely transform the user experience of standard websites (server-side generated or static ones) to make users feel like they are browsing an app, especially for those with low bandwidth connections.

{% note warning %}
Please use the absolute path of the image or [Hexo asset_img tag](https://hexo.io/docs/tag-plugins#Include-Assets) in your posts, otherwise the images may fail to load during Pjax refresh.
{% endnote %}

You can enable it by setting value `pjax` to `true` in {% label primary@theme config file %}.

```yml next/_config.yml
# Easily enable fast Ajax navigation on your website.
# For more information: https://github.com/next-theme/pjax
pjax: true
```

### Fancybox

NexT supports the fancybox plugin, which is a jQuery lightbox script for displaying images, videos and more. Touch enabled, responsive and fully customizable.

You can enable it by setting value `fancybox` to `true` in {% label primary@theme config file %}.

```yml next/_config.yml
fancybox: true
```

### Medium Zoom

[Medium Zoom](https://github.com/francoischalifour/medium-zoom) is a JavaScript library for zooming images like Medium.

You can enable it by setting value `mediumzoom` to `true` in {% label primary@theme config file %}.

```yml next/_config.yml
# A JavaScript library for zooming images like Medium.
mediumzoom: true
```

{% note warning %}
Do not enable both `fancybox` and `mediumzoom`.
{% endnote %}

### Lazyload

[Lozad.js](https://github.com/ApoorvSaxena/lozad.js) is a lazy loader plugin in modern vanilla JavaScript. It delays loading of images in long web pages. Images outside of viewport will not be loaded before user scrolls to them. This is opposite of image preloading.

You can enable it by setting value `lazyload` to `true` in {% label primary@theme config file %}.

```yml next/_config.yml
# Vanilla JavaScript plugin for lazyloading images.
lazyload: true
```

Then run the following command in {% label info@site root dir %} to ensure that `lazyload` can be enabled or disabled correctly:
```bash
$ hexo clean
```

### Pangu Autospace

[pangu.js](https://github.com/vinta/pangu.js) will automatically insert a blank space between all the Chinese characters and the hexagonal English numeric symbols on the page.

You can enable it by setting value `pangu` to `true` in {% label primary@theme config file %}.

```yml next/_config.yml
# Pangu Support
pangu: true
```

### Quicklink

[Quicklink](https://github.com/GoogleChromeLabs/quicklink) is a JavaScript plugin that faster subsequent page-loads by prefetching in-viewport links during idle time. Chrome, Firefox, Edge are supported without polyfills.

You can enable it by setting value `quicklink.enable` to `true` in {% label primary@theme config file %}.

```yml next/_config.yml
...
quicklink:
  enable: true
  home: true
  archive: true
  delay: true
  timeout: 3000
  priority: true
  ignores:
...
```

### Animation Effect

NexT enables animation effect by default which is supported by Anime.js and Animate.css, so it will wait for JavaScript loaded to show content.
If you need speed you can set the value of `motion.enable` to `false` to disable it.

Edit {% label primary@theme config file %} and set the needed values under the `motion` to fit your demand. You can preview all Transition variants here: [NexT Animation Effect Preview](https://theme-next.js.org/animate/).

```yml next/_config.yml
# Use Animate.css to animate everything.
# For more information: https://animate.style
motion:
  enable: true
  async: false
  transition:
    # All available Transition variants: https://theme-next.js.org/animate/
    post_block: fadeIn
    post_header: fadeInDown
    post_body: fadeInDown
    coll_header: fadeInLeft
    # Only for Pisces | Gemini.
    sidebar: fadeInUp
```

### Progress Bar

NProgress will automatically monitor your Ajax requests, event loop lag, document ready state and elements on your page to decide on the progress.

{% tabs nprogress %}
<!-- tab <code>nprogress</code> -->
You can enable it by setting value `nprogress.enable` to `true` in {% label primary@theme config file %}.

```yml next/_config.yml
nprogress:
  enable: true
```
<!-- endtab -->
<!-- tab <code>spinner</code> -->
Turn off loading spinner by setting it to `false`.

```yml next/_config.yml
nprogress:
  spinner: false
```

<!-- endtab -->
{% endtabs %}

### Canvas Ribbon

[canvas-ribbon.js](https://github.com/hustcc/ribbon.js) is a ribbon backgroud of website draw on canvas.

You can enable it by setting value `canvas_ribbon` to `true` in {% label primary@theme config file %}. You can also configure the ribbon setting by editing values in `canvas_ribbon` section:

* size: The width of the ribbon.
* alpha: The transparency of the ribbon.
* zIndex: The display level of the ribbon.

```yml next/_config.yml
canvas_ribbon:
  enable: true
  size: 300
  alpha: 0.6
  zIndex: -1
```
