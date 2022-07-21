#### Add normalize.css

- npm install normalize.css

#### SASS variables

- @import rather than @use is used in vite

Error: LF will be replaced by CRLF the next time Git touches it
Fix: git config --global core.autocrlf false

#### Button

declare padding

display: inline-block - the top and bottom margins/paddings are respected, but with display: inline they are not.

text-decoration: none - removes the underline

btn - Block
btn--orange -Block and Modifier

#### Mobile first

- if the screen is larger than 530px

```
@media(min-width: 530px){

    }
```

#### Mixins

base/\_mixins.scss

```
@mixin atSmall($font) {
  @media (min-width: 530px) {
    font-size: $font;
  }
}
```

modules/\_large-hero.scss

```
 @include atSmall(4.8rem);
```

#### Responsive Images

- the way image is cropped
- send different image files

###### Responsive image situations

1. Art direction & cropping situation

```
<picture>
    <source srcset="images/dog-crop-large.jpg" media="min-width:1200px" />
    <source srcset="images/dog-crop-medium.jpg" media="min-width:760px" />
    <img src="/images/dog-crop-small.jpg" alt="puppy" />
</picture>
```

Note:

> source media query 760px and above use medium image
> min-width means minimum width and above value

2. Image resolution & size situation (faster load times)

- image source and width assign - browser will automatically decide

```
 <img
      src="/images/dog-crop-small.jpg 570w,/images/dog-crop-medium.jpg 1200w,/images/dog-crop-large.jpg 1920w"
      alt="puppy"
 />
```

---

Add border bottom to .large-hero
.large-hero\_\_image - display to block
