# Flex-line height:

Single-line row flex container with definite height: <br>
flex-line height = container's inner height.

Items with height:auto: <br>
can stretch to the line height.

Items with fixed height: <br>
keep their own height and are aligned inside the line.

Demo: https://codepen.io/csspractice/pen/vEgdQqG

# Flex-basis, width:

width = usual element width <br>
flex-basis = starting main-axis size in Flexbox

If flex-basis is auto, Flexbox consults width. <br>
If flex-basis has a value, it takes priority for flex sizing.

# align-items:

align-items default = stretch

stretch only stretches flex items whose cross-size is auto.

If height is set in row flex, stretch will not override it. <br>
If width is set in column flex, stretch will not override it.

# align-content:

Multiple flex lines + fixed container height <br>
→ align-content becomes important.

Default align-content: stretch <br>
→ stretches the line boxes.

Fixed-height items <br>
→ do not stretch with the line boxes.

demo: https://codepen.io/csspractice/pen/jEyZRQd

# flex-wrap:

With flex-wrap: wrap:

Items start from their flex-basis.
If flex-basis:auto and no width is set,
that starting size is content-based, often similar to max-content.

But they are not guaranteed to stay max-content.
They can shrink because flex-shrink:1.
They overflow only after they cannot shrink further.

nowrap → try to fit all items in one line by shrinking them

wrap → use starting sizes to form multiple lines,
       then flex/shrink items within each line

The flex sizing process:  Demo: https://codepen.io/csspractice/pen/OPWvyNP
                                https://codepen.io/csspractice/pen/MYJVwaW

Simplified algorithm:

1. Give every item a starting size from flex-basis.

2. Add all item sizes + gaps.

3. Compare with container size.

4. If there is extra space:
   flex-grow distributes it.

5. If there is not enough space:
   flex-shrink reduces item sizes.

6. min-width, max-width, min-height, max-height can limit the final size.

flex-basis: auto; // means use width/height if provided <br>
                  // otherwise use content-based size 
```CSS
.item {
  width: 300px;
  flex-basis: 200px; /* starting size will be 200px */
}
```

flex: grow shrink basis;