stacked selectors use commas to influence multiple elements.

wheras descendent selectors use spaces to create a nested selector that is more highly specific.

can use this to combine rules

'>' is the direct descendent. selects children a single layer deep.

ex: .container > ul {
  //some style
}

+ is the adjacent selector

~ a sibling combinator

Combining selectors:

.peeka:hover + .boo {
  display: block;
}



When the element with a peeka class is hovered over, the item with a boo class immediately following it will have this style applied.


Rem vs em:

stands in relationship to the parent elements font-size property.

if none is given, it is 16px.

rem: root em. Relates back to font-size defined in root element which should generally be the html tag.

you can use inherit for all kinds of things, not just margin and padding! you can inherit all kinds. like borders!

margin, border, padding, content.

my brother programs computers.

padding order of values:


top, right, bottom, left.

t r b l (TRouBLe).



inline-block has functionality between inline and block. It flows with text, but it can be given a width and height like block elements, which doesn't work for regular inline elements.


Floats

* float specifies whether it should be placed along left or right of container


floats don't actually "wrap" so much as they move underneath items with the float property. except that text won't move underneath, even if the box that contains it does!

https://youtu.be/LrdkRMZhgZg

clear always has a new inline
forces a new line
clear both: clears both left and right floats.

clearfix with an empty div is not semantic!

https://youtu.be/dJt2PjybuQs
using :after is a semantic solution

this is a semantic clearfix:

.cf:after {
  content:"";
  display:table;
  clear: both;
}

## Positioning

4 kinds: static, relative, absolute, fixed.

static is default positioning, i.e natural document flow.

everything else is a positioned element.

relative: relative to containing element

absolute: relative only to pixel 0,0 of the browser window

fixed: same as absolute but does not scroll

Colllapsed margins: when tw margins touch and compound each other.

solution: only use margins on one side for everything!



Box sizing:

Generally a  good idea to add

* normalizer
and


`* html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}``

Building stylesheets outside -> in

- the content on this was confusing.
- look this up.
- also CSS Design patterns.


## Flexbox

https://youtu.be/G7EIAgfkhmg


## Pseudo-classes vs. pseudo-elements

:after is a pseudo class, it allows for styling to happen in such a way that it relates to the previous class.

::after is a pseudo-element. By setting the content property, you can actually insert content, not just styling, after the current element.


## Webkit prefixes

Android: -webkit-
Chrome: -webkit-
Firefox: -moz-
Internet Explorer: -ms-
iOS: -webkit-
Opera: -o-
Safari: -webkit-

## There is also an autoprefixer that is a css postprocessor


## Sass

What is a mixin goddamnit?

A mixin is a sass function or prototype!!

A mixin can take an argument!
