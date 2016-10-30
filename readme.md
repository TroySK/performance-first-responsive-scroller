# Performance-First Responsive Scroller

This is a simple Responsive Scroller for products. It may have any number of items and can responsively show different number of items on different resolutions.

After looking for multiple product scrollers and carousels; I built this with the primary goal of performance. Animations can be added via CSS transitions. Autoplay can be disabled by setting data-scroll to 0. It takes values in milliseconds.

In ideal situations, the CSS should be part of your Critical Path and the JavaScript may be lazily loaded. You may also want to autoprefix the CSS.

No JavaScript or CSS library required!

```
<div class="scroller" data-scroll="5000">
  <a href="#" class="left">	&lsaquo;</a>
  <div class="scroller-inner">
    <div class="scroller-item">1</div>
    <div class="scroller-item">2</div>
    ...
  </div>
  <a href="#" class="right">&rsaquo;</a>
</div>
```
Change the values in the responsive queries to get the correct number of elements in the desired resolution.

```
@media (min-width: 481px) and (max-width: 640px) {
  .scroller-item {
    width: calc(50% - 2rem);
  }
}
@media (min-width: 641px) and (max-width: 960px) {
  .scroller-item {
    width: calc(33% - 2rem);
  }
}
@media (min-width: 961px) and (max-width: 1200px) {
  .scroller-item {
    width: calc(25% - 2rem);
  }
}
@media (min-width: 1201px) {
  .scroller-item {
    width: calc(16.67% - 2rem);
  }
}
```
