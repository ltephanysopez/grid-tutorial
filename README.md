#📓 CSS GRID TUTORIAL
You can see the layout in action here: https://ltephanysopez.github.io/grid-tutorial/

## 👩🏽‍💻 _Hi! This tutorial showcases how to create responsive web layouts with CSS Grid._


Chances are, I've either directed you here, or you've been spelunking through my GitHub repos: in which case, welcome! This tutorial assumes you have some fundamental knowledge of HTML/CSS, but if you don't, that's perfectly fine!

***************

### `CSS GRID`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://pbs.twimg.com/media/Dp6psotU0AELSum.jpg:large" height=220>

CSS Grid is a technique in CSS that allows developers to create responsive web design layouts more easily and consistently across browsers.

## Getting started
Let's create a container that holds a couple of items in our HTML.
```
<div class="grid">
  <div class="item-1">1</div>
  <div class="item-2">2</div>
  <div class="item-3">3</div>
  <div class="item-4">4</div>
  <div class="item-5">5</div>
  <div class="item-6">6</div>
  <div class="item-7">7</div>
  <div class="item-8">8</div>
  <div class="item-9">9</div>
</div>
```

To turn our container into a grid, we simply give it a `display` of grid:
```
#grid {
    display: grid;
}
```
Because we haven't defined any grid properties yet, our current grid will simply stack all items on top of each other.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://pbs.twimg.com/media/Dp6zhfzUcAAVfvb.jpg:large" height=320>

## Creating a two-dimensional layout
To make a two-dimensional layout, we’ll need to define the columns and rows. For this example, we'll create three columns and two rows by using the `grid-template-row` and `grid-template-column` properties.

```
#grid {
    display: grid;
    grid-template-columns: 100px 100px 100px;
    grid-template-rows: 50px 50px;
}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://pbs.twimg.com/media/Dp60UknUwAEnKcq.jpg:large" height=320>



Using the same markup with different values, let’s create a 3x3 grid.
```
#grid {
    display: grid;
    grid-template-columns: 100px 100px 100px;
    grid-template-rows: 100px 100px 100px;
}
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://pbs.twimg.com/media/Dp602cFU4AA44z2.jpg:large" height=320>


## Position and Resizing
To position and resize the items we’ll target them and use the grid-column and grid-row properties, which define items by grid _lines_:
```
.item-1 {
    grid-column-start: 1;
    grid-column-end: 4;
}
```
The markup above says that the first item will span from column line 1, and end at column line 4. In other words, it’ll take up the entire row. Here’s how that’ll play out on the screen:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://pbs.twimg.com/media/Dp66YO3UwAAYJXv.jpg:large" height=320>


*****************
