# DirtyScript.js
Javascript framework for building html with easier and more readable way using **tree objects**
> This is kinda like dart with flutter but easier

### **you need to use `type="module"` for this to work**

> Setup index.html by importing your `main.js` as an module
###
> then download this git as **dscript** folder
# index.html
```html
<body>
    ...
    <div id="root"></div>
    <script src="main.js" type="module"></script>
</body>
```

# main.js
```js
import { dScript } from "./dscript/dscript.js";
import { global } from "./dscript/frawem.dscript.js";

const code = `
html(
  text("Hello World")
)
`

eval(dScript.create(code))
```

### now after setuping out workspace, let's dive in even further
```js
// lets build some containers
const code = `
html(
    box(
        text("hello")
        text("world")
    )
)
`
```

```js
// and maybe some rows and collumns...
const code = `
html(
    row(
        text("Hello ")
        text("World")
    )
    column(
        text("Hello ")
        text("World")
    )
)
`
```

```js
// now use something more useful
const code = `
html(
    column(
        start(
            text("im at the start")
        )
        center(
            text("im centered!")
        )
        end(
            text("im at the end!")
        )
    )
)
`
```


```js
// to make it more fun we can use customization
// :color() is kinda like text_style.color() 
// why text_style tho? because : refer to atribute given by its parent
// in the line with :color(), the parent was text_style
const code = `
html(
    text(
        text_style(
            :color("red")
        )   
        "I have red colour!"
    )
)
`
```

```js
// noticed we didnt used text(...) in previous code, that's because we dont need text() if the string is in the last parameter/child
// let's use another example
const code = `
html(
    box(
        :class("myTitle")
        :background("blue")
        text(
            text_style(
                :size("40px")
            )
            "My website's title"
        )
    )
)
`
```

```js
// now after knowing the basics, here is some example app
const code = `
html(
    box(
        :background("#222")
        :padding("8px")
        text(
            text_style(
                :size("40px")
            )
            "My Website"
        )
    )
    box(
        :padding("18x")
        center(
            column(
                :gap("12px")
                text("Hi")
                text("Hello")
                text(
                    // we can use String() to stringify math expressions
                    String(1+1)
                    text(" - is the result of 1+1")
                )
            )
        )
    )
)
`
```
