# Hack CSS

Collection for css hack in different browsers. Provide a easy way to take css hack.

### less

require less v1.7.0 or later

```less
@import "path/to/hack-css.less"

// give hack for each selector which you need
.class {
    .hack-css-ie6({
        hasLayout: 1;
    })

    .hack-css-ie7({
        margin: 0;
    })
}

// give hack for all selector together
@hack-css-ie6: {
    .class {
        hasLayout: 1;
    }

    #id {
        padding: 0;
    }
}
```

### stylus

```stylus
// use block to give hack to all, but you should require after
hack-css-ie6 = 
  .class 
    hasLayout 1
  #id
    padding 0

@require 'path/to/hack-css'
```

```stylus
// use block mixin to hack each selector
@require 'path/to/hack-css'

.class
  +hack-css-ie6
    hasLayout 1
  +hack-css-ie7
    padding 0
```

### sass & scss

```sass
// hack each selector
.class {
    @include hack-css-ie6 {
        hasLayout: 1;
    }
}

// hack all selector
@include hack-css-ie6 {
    #id {
        hasLayout: 1;
    }
}
```

```scss
.class
  +hack-css-ie6
    hasLayout: 1

+hack-css-ie6
  .class 
    padding: 0
```

## API list
```
```

## Reference

- [css hacks](http://www.paulirish.com/2009/browser-specific-css-hacks/)  
- [media blocks hacks](http://keithclark.co.uk/articles/moving-ie-specific-css-into-media-blocks/) 
- [conditionnal stylesheets vs css hacks](http://www.paulirish.com/2008/conditional-stylesheets-vs-css-hacks-answer-neither/)  
