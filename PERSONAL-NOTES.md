# CSS drafts

- `keyframes`: `opacity` and `transform` are the only properties that are optimized in browsers and should be used in keyframes
- `h1` is very important for SEO; it should contain webpage title and what about the page is
- `display: block` - utilizes the whole available width and applies line breaks
- properties related to `font` are inherited; `padding` is not
- `span` - used when you want to style texts differently
- reset universal selector:

```css
*::after,
::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}
and
body {
  box-sizing: border-box;
}
```

- `backface-visibility: hidden` - hides a element's background during animations; good fix for shaking effect
- good practice in giving CSS classes to elements: `btn btn-green`; `btn` class defines common properties for all buttons, `btn-green` class defines green color of the specific button
- centering options:
  - `absolute` with `transform: translate` child + closest `relative` parent is a reference (texts)
  - `display: inline-block` child + `text-align: center` parent (buttons - treated as inline text);
  - `absolute` with `top: 0; left: 0` child + closest `relative` parent is a reference
  - `margin: 0 auto` center block element inside another block element
- `padding` - inside element (button shape)
- `margin` - whitespaces (between elements)
- pseudo-classes - states
- `transition: all` - easier version of `animation`; used in initial state (e. g. visited pseudo-class) to tell that all properties (states) are enabled for animations
- `after` pseudo-element - has to have `content` and `display` element  (even empty); treated like a child of the element
- fade in/out effect: `transition: all Xs` + `opacity: 0` in e. g. hover pseudo-class
- `animation-fill-mode: backwards` - applies effects from `0%` state before a delayed animation starts
- root font size: `html { font-size: 62.5% }` (by default results in 10px font size)
- Layout: Component-Driven Design, Atomic Design (Brad Frost)
- Naming classes: BEM, OO CSS, Smacss
- Architecture: 7-1 Pattern, ITCSS, Smacss
- fix for collapsed child elements when using float in parent which results in 0 height:

```css
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
```

- responsive design principles
  - fluid grids and layouts - using % instead od px for lengths, especially for widths
  - flexible/responsive images - dimension usually defined in %
  - media queries - changing styles on certain viewport widths (breakpoints)
- layout types
  - float layouts - boxes side by side using float
  - flexbox - laying elements in 1-dimensional row
  - CSS grid - laying elements in 2-dimensional grid  

- standard row width in grid - `max-width: 1140px` (in rems)
- `calc` function - in native CSS can contain mixed units, in SCSS cannot (in preprocessing stage Sass does not know what % and rem is)
- `main` - HTML5 element, tells websites it is main part of our site
- `background-image: linear-gradient(to right, color1, color2); -webkit-background-clip: text; color: transparent;`
- `transform: skewX(1deg)`
- `.u-center-text { text-align: center }`
- arrow symbol: `&rarr` (HTML entities)
- show back side of a card: `transform: rotateY(-180deg); perspective: 150rem; -moz-perspective: 150 rem;`, perspective should be in a parent element, the bigger value the more smooth the effect is, teh best way is to experiment a little bit, child should has `backface-visibility: hidden`
- fix for collapsed height of parent when we give `position: absolute` to children - give the same height to the parent that children have
- `background-blend-mode: screen`
- fix for child overlapping parent - `overflow: hidden`
- `clip-path: polygon(...)`, copy-paste `-webkit-...` for support in all browsers
- `test-transform: uppercase;`
- `box-decoration-break: clone` - applies all decorations of an element to all elements created by this element (e. g. padding), need copy-paste of `-webkit-...`
- `border-top-left-radius: 3px` - rounding of one corner
- `shape-outside`, element has to be floated
- `filter` - blur, brightness
- `object-fit: cover` - pretty similar to `background-size: cover`, fill does not remain aspect ratio

## Flexbox

## CSS Grid
