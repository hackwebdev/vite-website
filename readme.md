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
@mixin atSmall {
  @media (min-width: 530px) {
    @include atSmall;
  }
}
```

modules/\_large-hero.scss

```
 @include atSmall {
      font-size: 4.8rem;
    }
```
