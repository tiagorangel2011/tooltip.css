# Positioning
For positioning, use data-tooltip-pos attribute with one of the values:
up, down, left, right, up-left, up-right, down-left, or down-right.

```
<button aria-label="Whats up!" data-tooltip-pos="up"></button>

<button aria-label="Whats up!" data-tooltip-pos="left"></button>

<button aria-label="Whats up!" data-tooltip-pos="right"></button>

<button aria-label="Whats up!" data-tooltip-pos="down"></button>

<button aria-label="Whats up!" data-tooltip-pos="up-left"></button>

<button aria-label="Whats up!" data-tooltip-pos="up-right"></button>

<button aria-label="Whats up!" data-tooltip-pos="down-left"></button>

<button aria-label="Whats up!" data-tooltip-pos="down-right"></button>
```

# Length
By default, tooltips will always remain single-line no matter their length. You can change this behavior by using the attribute data-tooltip-length with one of the values: small, medium, large, or fit.

```
<button data-tooltip-length="small" aria-label="Hi." data-tooltip-pos="up">I'm a medium tooltip</button>
I'm a small tooltip
<button data-tooltip-length="medium" aria-label="Now that's a super big text we have over here right? Lorem ipsum dolor sit I'm done." data-tooltip-pos="up">I'm a medium tooltip.</button>
I'm a medium tooltip.
<button data-tooltip-length="large" aria-label="What about something really big? This may surpass your window dimensions. Imagine you're in that boring class with that boring teacher and you didn't sleep so well last night. Suddenly you're sleeping in class. Can you believe it?!" data-tooltip-pos="up">I'm a large tooltip</button>
I'm a large tooltip
<button data-tooltip-length="xlarge" aria-label="What about something really big? This may surpass your window dimensions. Imagine you're in that boring class with that boring teacher and you didn't sleep so well last night. Suddenly you're sleeping in class. Can you believe it?!" data-tooltip-pos="up">I'm a Xlarge tooltip</button>
I'm an Xlarge tooltip
<button data-tooltip-length="fit" aria-label="What about something really big? This may surpass your window dimensions. Imagine you're in that boring class with that boring teacher and you didn't sleep so well last night. Suddenly you're sleeping in class. Can you believe it?!" data-tooltip-pos="up">My width will fit to element</button>
```

# Disabling animation
If for some reason you do not want animations in your tooltips, you can use the `data-tooltip-blunt` attribute for that.

`<button data-tooltip-blunt aria-label="No animation!" data-tooltip-pos="up">No animation!</button>`

# Showing tooltips programmatically
If you want to show tooltips even when user interaction isn't happening, you can simply use the data-tooltip-visible attribute:

`<button data-tooltip-visible aria-label="I am always visible!" data-tooltip-pos="up">Always visible!</button>`
The attribute data-tooltip-visible can be easily added via JavaScript (e.g. .setAttribute()), enabling you to show tooltips whenever needed.

# Customizing Tooltips
Tooltip.css exposes three CSS variables to make it easier to customize tooltips: --tooltip-color, --tooltip-font-size and --tooltip-move. This way you can use custom CSS to make your own tooltip styles:

```
/* Add this to your CSS */
.tooltip-red {
  --tooltip-color: red;
}

.tooltip-big-text {
  --tooltip-font-size: 20px;
}

.tooltip-slide {
  --tooltip-move: 30px;
}
```

```
<button aria-label="I am red!" class="tooltip-red">I am red!</button>
<button aria-label="I have big text!" class="tooltip-big-text">I have big text!</button>
<button aria-label="I move a lot!" class="tooltip-slide">I move a lot!</button>
```
You can combine classes to achieve multiple customizations. If you want to customize tooltips globally, use the :root selector:

```
/* All tooltips would now be blue */
:root {
  --tooltip-color: blue;
}
```
# Glyphs and Icon Fonts
You can also add any HTML special character to your tooltips, or even use third-party Icon fonts:

```
<button aria-label="HTML special characters: &#9787; &#9986; &#9820;" data-tooltip-pos="up"></button>

<button aria-label="Emojis: 😀 😬 😁 😂 😃 😄 😅 😆" data-tooltip-pos="up"></button>

<button class="font-awesome" aria-label="Font Awesome: &#xf030; &#xf133; &#xf1fc; &#xf03e; &#xf1f8;" data-tooltip-pos="up"></button>
```

Thanks for reading! To learn more please visit https://tooltipcss.glitch.me/.
