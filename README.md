# dirty-script
Javascript framework for building html with easier and more readable way

### **you need to use `type="module"` for this to work**

## Setup index.html by importing your `main.js`
```html
<body>
    ...
    <script src="main.js" type="module"></script>
</body>
```

# Setup main.js
```js
import { dScript } from "./dscript/dscript.js";

var code = `
html(
  text("Hello World")
)
`

eval(dScript.create(code))
```
