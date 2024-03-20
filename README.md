# Font Awesome Custom Icon Demo
> This project started as a fork of [fa-custom-icon-demo](https://github.com/mlwilkerson/fa-custom-icon-demo).

> You may have to to your own ``script`` and ``link`` tags. For details, see the comment in ``index.html``.

This demo shows how you can add a custom font to FontAwesome, all in plain ``JavaScript``.

## Step by step guide

1. Use your favorite tool to create your icon.
2. Save it as an SVG.
3. Open the SVG with a text editor, and look for the `d=` attribute of the `<path>`.
4. Create and export a plain JavaScript object in your own custom icon pack file similar to the `faSplat` sample in `custom-icon-pack.js`.
5. Paste the svg path data into the same place in that JavaScript object as you see the svg path data in the `faSplat` sample.
6. Set the remaining properties of that JavaScript object as follows:

```javascript
export const faSomeObjectName = {
  // Use a prefix like 'fac' that doesn't conflict with a prefix in the standard Font Awesome styles
  // (So avoid fab, fal, fas, far, fa)
  prefix: string,
  iconName: string, // Any name you like
  icon: [
    number, // width
    number, // height
    string[], // ligatures
    string, // unicode (if relevant)
    string // svg path data
  ]
}
```

## SVG tools
There are a lot of online and offline tools to create SVGs.

Here is a list of offline tools.
1. [GNU Image Manipulation Program (GIMP)](https://www.gimp.org/)
2. [INKSCAPE](https://inkscape.org/?switchlang=en)

Of course you can also import an existing SVG and edit it to your liking, with for example GIMP. Simply open GIMP,
go to the paths panel (if not visible, go to ``Windows`` > ``Dockable Dialogs`` > ``Paths`` to enable it) and then
right click in the paths panel and click ``Import Path``. After that, you can navigate to your SVG and click
``open``.
When you are done with your modifications, you again do a right click and then click ``Export Path`` to export it to a SVG.
As a tip, you can also merge paths by simply making all the paths you want to merge visible, and then again right click
in the paths panel and click ``Merge Visible Paths``.

And here is a list of offline tools.
1. [yqnn](https://yqnn.github.io/svg-path-editor/)

There is also a tool called [icomoon](https://icomoon.io/app/#/select) where you can upload a SVG and download it as a ``JSON``.
