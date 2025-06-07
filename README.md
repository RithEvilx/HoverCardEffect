# HoverCardEffect

This project demonstrates the use of advanced CSS selectors:

1. The adjacent sibling combinator " + "
2. The universal selector " \* "
3. The pseudo-class " :has() "

---

## CSS Explanation:

1. .item:has(+ \*:hover)
   => Selects an .item element if the next sibling (any type) is being hovered.
   => In simple terms: "If the box AFTER me is hovered, I get styled."

2. .item:hover + \*
   => Selects the next sibling of the currently hovered .item, no matter the tag/class.
   => In simple terms: "When I hover this box, the box AFTER me gets styled."

## Example in HTML:

<div class="list">
  <div class="item"><img src="img/img1.jpg" style="width: 200px"/></div>
  <div class="item"><img src="img/img2.jpg" style="width: 200px"/></div>
  ...
</div>

## CSS Example:

.list .item:has(+ \*:hover) {
filter: brightness(0.6);
transform: rotateY(-40deg);
}

.list .item:hover + \* {
filter: brightness(0.6);
transform: rotateY(40deg);
}

## Behavior:

- Hover an item:
  => The NEXT item gets dimmed and rotated to the right.
  => The PREVIOUS item also gets dimmed and rotated to the left.

## Browser Support:

- ✅ Chrome 105+
- ✅ Safari 15.4+
- ❌ Firefox (not supported yet)

Created by RithEvil!
Date: 07 June 2025
