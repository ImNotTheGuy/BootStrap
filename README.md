# Introduction to bootstrap

Helps the developer avoid spending too much time on design and writing CSS. It keeps a coherent design system accross the web/mobile - app

## Project organization

All CSS files will go in `css` folder:

New folder [vendor](/css/vendor/) where we put the CSS written by third parties

New folder [page](/css/page/) where we put the CSS specific to certain HTML pages.

New file [style.css](/css/style.css) where we'll put the CSS code shared throughout the webpages of our projects.

## Import Bootstrap in the HTML

To use the bootstrap CSS file, simply add a link to the head of the HTML:
`<link rel="stylesheet" href="/css/vendor/bootstrap.min.css">`

## Import Bootstrap using CDN

Same as above but replace the code with:

```
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx"
      crossorigin="anonymous"
    />
```

The advantage of CDN import is that the bootstrap file will be as close as possible as the client. This can reduce load time if for instance a French client requests a US server. The CDN bootstrap is hosted on multiple servers. Therefore the client will load the web page from the US server, but will load the CSS from it's French server. Can be meaningful for slower connections.

## Responsive Layout

Bootstrap can easily make a layout responsive. The layout will dynamically change depending on the screen size of the client.

### Bootstrap grid-layout

In bootstrap, the 3 blocks should all be child of the parent element, called the _container_.

The direct children of a container is called a _row_.

In each row, we can have different columns called a _col_.

Each element: `container`, `row` and `col` are the names used in Bootstrap

Tip: in VsCode with the .emmet extension, if you type `.row*3` for example, it will create 3 `<div>s` with the class row 3 times. you can also do it with multiple class at once: `.row.another-class*3`

### Overriding Bootstrap classes

To do that, add another `<link>` **below** the bootstrap the import and reference your own `style.css` file, as follows:

`<link rel="stylesheet" href="/css/style.css">`

Then, write normal CSS referencing the same name of the class you wish to override. For example:

```
.row{
    margin: 10px;
    padding: 15px;
    background-color: lightblue;
}
```

This will override the `row` class of bootstrap on defined attributes, but will keep it's core working.


### Combining multiple classes

In our example, we can combine the `col` class with a personal class called `topic`. This will keep the grid-layout of the `col` class but will add caracteristics of the `topic` class: `<div class="col topic">`


tip: *on Firefox, to change the layout to mobile devices, use *`CTRL + SHIFT + M` *and select the device you want* 


### Bootstrap grid layout specifications

By default, 1 `row` is comprised of 12 `col`. If you have only 4 elements, each `col` will actually be 3 columns.

To override this, you can specify how many columns for each `col` element you want using: `<div class="col-n">`

For different screen types, you can specify the behaviour of the layout by using screen size suffixes 
- `-lg`: large
- `-md`: medium
- `-sm`: small
- `-xs`: extra-small

Used as follows: `<div class="col-lg-3 col-md-6 col-sm-9 col-xs-12"> `