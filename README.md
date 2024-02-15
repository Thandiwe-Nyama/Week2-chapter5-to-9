# Week2-chapter5-to-9
HTML Working with Graphics and Images
Images When we want to add an image to a webpage, we use the image element, which is simply written as IMG. 
<img src="image.jpg" alt="image" width="200" height="100">
there are four attributes that need to be included for every image: First, we have the source attribute (SRC), which tells the browser which image file to load. 
Then we have the alt attribute (ALT), which provides a text description of the image. 
Lastly, we have the width and height attributes, which determine the size of the image. So, every image should have all four of these attributes.

Image Formats
It needs to be in a file format that web browsers can understand, and there are various options available. 
There are four main file formats commonly used on the web these days, each with its own strengths and weaknesses when it comes to compressing images. 
GIF
SVG
JPG
PNG

Responsive Images
HTML allows us to deliver different image files to screens of different sizes. We can create multiple image files and include them as options in our HTML code. Then, the browser, in collaboration with the operating system, takes into account the device's hardware capabilities and network speed to decide which image to download. 

Responsive Width
This is similar to the previous one, where there were four images listed in the src set attribute. But instead of specifying the pixel density like one x, two x, etc., indicate the width of each file: 480w for 480 pixels wide and 960w for 960 pixels wide.
The browser now decides which image to show based on device density and viewport width. This can lead to a problem where the chosen image does not fit the layout you want. The browser makes this decision early in the loading process, before it knows the CSS or layout details. It does not know the size of the box where the image will go. 
 Use the sizes attribute in HTML to specify which image to use at different breakpoints. This way, the browser can download the right-sized image for your layout. HTML has powerful options like src set, where we can provide a set of images for different resolutions or let the browser choose based on density and viewport width. The sizes attribute allows us to specify how much of the viewport's width the image will take up at each 
Responsive Pictures  To start off, use the image element with its ALT text and a URL to the image file. This ensures that even outdated browsers like Internet Explorer 11 can display the image. Now, wrap this image element with the picture element. This acts as a wrapper for the whole setup. Within the picture element, list alternative options using the source element. In this instance, provide two options by creating two source elements.

For the first source element, use the source set attribute to point to a mobile image file. This will be the cropped version of the photo, sized at 320 pixels wide. This way, when the viewport is smaller than 600 pixels, this version of the photo will be loaded.
In the other source element, use a kind of media query to specify the image for larger screens. When the viewport is at least 600 pixels wide, the landscape version of the photo will load. This is a pretty neat trick that allows you to optimize the image for different screen sizes.
