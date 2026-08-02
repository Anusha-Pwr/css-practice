# auto-fit vs auto-fill:

auto-fill: <br>
Make as many tracks as can fit.
Keep empty tracks too.
With minmax(200px, 1fr), extra space is shared among all tracks, including empty ones.

auto-fit: <br>
Make as many tracks as can fit.
Collapse empty tracks.
Extra space is shared among the tracks that actually have items.

Demo: https://codepen.io/csspractice/pen/BypxpxN

# 1fr 1fr vs 50% 50% vs auto auto 

1fr 1fr: <br>
gap removed first, leftover divided equally.

50% 50%: <br>
percentages calculated first, gap added after, can overflow.

auto auto: <br>
columns start from content size.
gap is accounted for.
leftover may stretch auto tracks unless you use justify-content: start.
auto does not mean the text cannot wrap, it is NOT like max-content.

Demo: https://codepen.io/csspractice/pen/BypxRxG

# justify-content: normal

100px 100px → fixed tracks, no stretching <br>
1fr 1fr    → flexible tracks, divide leftover space <br>
auto auto  → content-sized tracks, but can stretch by default

# Implicit grid

Explicit grid: <br>
Rows/columns you define using grid-template-columns and grid-template-rows.

Implicit grid: <br>
Extra rows/columns Grid creates automatically when items do not fit inside the explicit grid.

grid-auto-rows: <br>
Controls height of automatically created rows.

grid-auto-columns: <br>
Controls width of automatically created columns.

Demo: https://codepen.io/csspractice/pen/PwWeeWG





