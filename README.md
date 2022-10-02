# Hamburger

A simple hamburger component, It can be easily modified and used for your project, A complete guide about how to build this project from scratch is covered in this [Youtube video](https://www.youtube.com/)

### Recommended sizes

If you intend to use the hamburger component for your project the 150px width and height might just be too big unless you are building for ultra wide screens, Below we have compiled a width and height that would be suitable for most mobile devices, you can decide to use them or follow the guide in deciding what size works best for you.

```css
.hamburger {
  width: 45px;
  height: 45px;
}
```

You might just notice that after reducing the hamburger menu's size the vertical spacing between the bars are just too much, you need to reduce the translateY values so they can match your hamburger;

```css
.bars::before {
  transform: translateY(-8px);
}
.bars::after {
  transform: translateY(8px);
}
```

This fixes it for the most part, You can decide to come with up with your values, remove the background and border radius if your project deos not require them.
## Fast Lane
For users that just want to use this component right away, just copy the HTML, CSS and Javascript Snippet below and ensure you link them properly and everything should work just fine, If you chang the class names, ensure to update them in the HTML,CSS and JS files respectively. You can watch the full video of how to build this project [Here](https://www.youtube.com/)

### HTML

```html
 <div class="hamburger" onclick="toggleClassName()">
     <div class="bars"></div>
 </div>

```
### CSS

```css

.hamburger {
    width: 45px;
    height: 45px;
    background: #215ff6;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;

}

.bars {
    background: #fff;
    height: 3px;
    width: 60%;
    position: relative;
}

.bars::before {
    content: '';
    width: 100%;
    height: 3px;
    background: #fff;
    position: absolute;
    transform: translateY(-8px);
}

.bars::after {
    content: '';
    width: 100%;
    height: 3px;
    background: #fff;
    position: absolute;
    transform: translateY(8px);

}

.crossburger .bars {
    background: transparent;
}

.crossburger .bars::before {
    transform: translateY(0px) rotate(45deg);
}

.crossburger .bars::after {
    transform: translateY(0px) rotate(-45deg);

}


```
### JS

```javascript

var hamburgerdiv = document.querySelector(".hamburger")
function toggleClassName() {
    hamburgerdiv.classList.toggle('crossburger')
}

```
## License

Hamburger is licensed under the [MIT license](http://opensource.org/licenses/MIT).

## Related

- [Animated Hamburger](https://github.com/Xeraxlabs/hamburger-animated)
