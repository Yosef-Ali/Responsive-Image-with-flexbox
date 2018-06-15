# Responsive-Image-with-flexbox
Responsive image with flexbox layout page best code from Tania https://www.taniarascia.com/how-to-build-a-responsive-image-gallery-with-flexbox
## Grid
Make sure before starting to include some sort of reset, or at least set `box-sizing: border-box` and `margin: 0` to the body.
## Mobile
Mobile first layout means utilizing min-width @media queries for bigger screen sizes.
```
.container {
  margin: 0 auto;
  max-width: 1200px; /* any size */
  padding: 0 1rem;
}
```
Make the image responsive by putting a `max-width` on it.
````
.responsive-image {
  max-width: 100%;
}
````
image should be a `block` level element.
```
.cell img {
  display: block;
}
```
## Tablet

Choose 600px as the width to start showing the mid-screen view. We want the images to show up in rows of two now.
```
@media screen and (min-width: 600px) {
  .grid {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
  }
  .cell {
    width: 50%;
  }
}
```
## Desktop

At 1000px, show the desktop view, which will display the images in rows of three. 
```
@media screen and (min-width: 1000px) {
  .cell {
    width: calc(100% / 3);
  }
}
```
