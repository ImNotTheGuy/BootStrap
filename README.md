# Introduction to bootstrap

Helps the developer avoid spending too much time on design and writing CSS. It keeps a coherent design system accross the web/mobile - app 


## Project organization

All CSS files will go in `css` folder:

New folder [vendor](/css/vendor/) where we put the CSS written by third parties

New folder [page](/css/page/) where we put the CSS specific to certain HTML pages.

New file [style.css](/css/style.css) where we'll put the CSS code shared throughout the webpages of our projects.

## Import bootstrap in the HTML

To use the bootstrap CSS file, simply add a link to the head of the HTML:
 ```<link rel="stylesheet" href="/css/vendor/bootstrap.min.css">```

 ## Import bootstrap using CDN

 Same as above but replace the code with: 

```
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx"
      crossorigin="anonymous"
    />
```







