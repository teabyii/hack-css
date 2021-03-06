# Hack CSS

Collection for css hack in different browsers. Provide a easy way to take css hack.

### less

require less v1.7.0 or later

```less
@import "path/to/hack-css.less"

// give hack for each selector which you need
.class {
    .only-ie6({
        hasLayout: 1;
    })

    .only-ie7({
        margin: 0;
    })
}

// give hack for all selector together
@only-ie6: {
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
$only-ie6 = 
  .class 
    hasLayout 1
  #id
    padding 0

@import 'path/to/hack-css'
```

```stylus
// use block mixin to hack each selector
@import 'path/to/hack-css'

.class
  +only-ie6()
    hasLayout 1
  +only-ie7()
    padding 0
```

```stylus
// if you want both
@import 'path/to/hack-css'
... // your code
@import 'path/to/hack-css'
```

> Note: Now don't support only-ie11, or-saf5-saf6, only-op, in the first way by stylus. If want to hack, please take the second way, sorry.

### sass & scss

```sass
// hack each selector
.class {
    @include only-ie6 {
        hasLayout: 1;
    }
}

// hack all selector
@include only-ie6 {
    #id {
        hasLayout: 1;
    }
}
```

```scss
.class
  +only-ie6
    hasLayout: 1

+only-ie6
  .class 
    padding: 0
```

## Hack list

- only-ie6
- only-ie7
- only-ie8
- or-ie6-ie7
- or-ie6-ie7-ie8
- or-ie8-ie9-ie10
- or-ie9-ie10
- only-ie11
- or-saf2-saf3
- or-saf5-saf6  
  safari 5.1 ~ safari 6
- only-ff  
  firefox 3.5+
- only-op  
  opera 9.5+

## Reference

- [all browsers hacks](http://browserhacks.com/)  
- [css hacks](http://www.paulirish.com/2009/browser-specific-css-hacks/)  
- [media blocks hacks](http://keithclark.co.uk/articles/moving-ie-specific-css-into-media-blocks/) 
- [conditionnal stylesheets vs css hacks](http://www.paulirish.com/2008/conditional-stylesheets-vs-css-hacks-answer-neither/)  
