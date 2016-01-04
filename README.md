# Wallaroo-Styles
Here I'll be posting snippets of CSS that we commonly use at Wallaroo.
We're breaking this down into the principles of Atomic design:
Atoms -> Molecules -> Organisms -> Templates -> Pages

The absolute highest this could ever get is with Organisms. Templates and Pages are too unique to each page to

##Basically
This is a simple repository that will be one part documentation, one part plugin. In the same vein as PostCSS this will be a plug-and-play CSS file.

##Atoms
###Letter Spacing
Typically Wallaroo uses two different letter spacings. This will vary on a case by case basis of course, but the following are good estimates to start off with.

###Image with a background shade
This is done by putting a background color on the figure and making the image slightly transparent. On hover of the figure, we make the image completely opaque.
NOTE: There is a display: block on the image. This is crucial because without it the div will expand past the transparent image, causing a strip of solid color on the bottom

###Text with borders
There are two different ways we can go about this to solve two different problems

+ If the line does not need to be the same length of the text
++ We will put hr elements before and after the text then size it appropriately
+ If the line needs to be the same length as the text
++ Use the border CSS properties. This requires a wrapper with display: block so that we can center it if that's needed. display: inline-block; is placed on the h3 so that the width of the borders confines to the width of the text.

##Molecules

###Text on Image

####Where there is an actual image
We do this with a figure and figcaption element. It simply requires repositioning of the figcaption to the desired space. Default is centered.

####Where it is a background image
The container element receives a relative position, the child element gets an absolute position and is placed directly in the middle.

###Image Grid
A simple grid of images with each one being 33% wide. There are two ways to do this layout, using inline-block and manually defining the width, or using flex-box. We steal the code from the Text on Image section to overlay the text

###Image Grid w/ color hovers
Our grid combined with the background shading

###Image Grid w/ color hovers and text borders
Our grid combined with the background shading and borders
