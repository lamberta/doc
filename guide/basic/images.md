# Images

## Using an ImageView

This example requires an image in your resources directory
and renders it to the screen.

~~~
m4_include(./examples/api/example-imageview.js)
~~~

Place this in the `Application.js` file of your project,
rotate the simulator, and you'll see:

<img src="./assets/ui-imageview/example-imageview.png" alt="a book screenshot" class="screenshot">


## Using 9-Slice Image Scaling

Given the following 300x300 image:

<img src="./assets/ui-imageview/button.png" alt="sample button image" class="screenshot">

We can scale it to the dimensions of the device (with a
slight centering for visibility) so that the rounded corners
maintain their integrity while the middle section is scaled
out. This way buttons can maintain their style despite the
dimensions of the device.

Here, the image is sliced and scaled out, and a label is
given to the button by assigning a `TextView` as a
child. The child view's dimensions is set to the width and
height of the middle section of the `ImageScaleView`, and
set to a very light blue so you can see it in the example
below. The debugging flag of the `ImageScaleView` is set to
`true` so you can see how the slices are sectioned off.

~~~
m4_include(./examples/api/example-imagescaleview.js)
~~~

Run this code as the `Application.js` file in your project,
and you should see something like this in the simulator:

<img src="./assets/ui-imageview/example-imagescaleview.png" alt="9-slice scaling screenshot" class="screenshot">

Click anywhere on the button background image with your
browser console open and you'll see the message.

If you change the dimensions of your device by clicking
**Choose Device** on the simulator screen, you will see that
the background image of the button scales appropriately,
while the button text remains centered on the screen.