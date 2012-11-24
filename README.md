html_style_guide
================
A dedicated style guide for HTML


## Rules:
1. Avoid div-itis and use new HTML tags such as (header, footer, aside, article, section)
2. Avoid the use of ID's except for when needed by JavaScript. You never know when you will need to re-use a style,
or adapt a style for another use.

## Tags:

Use the HTML <button> element when ever you are linking to elements (not content) on the same page when 
you are not using anchor tags to link to content. This is ideally used when opening up modals, dialogs.

```html
<button>Your Button</button>
```

## Menus
When coding a menu, it is important to wrap your menu items with the new HTML5 <nav> tag. Since navigation links are 
usually a list of links, it is important to place the menu items in a list.

General Menu
```html
<nav>
    <ul>
        <li>Menu Item 1</li>
        <li>Menu Item 2</li>
        <li>Menu Item 3</li>
    </ul>
</nav>
```

or

Organized Menu
``` html
<nav>
    <ol>
        <li>Menu Item 1</li>
        <li>Menu Item 2</li>
        <li>Menu Item 3</li>
    </ol>
</nav>
```


## Attributes:
### alt=''
All images which are using the <img> tag should use the alt attribute. If not alternative is provided, it is still 
recommened to use the alt attribute but with an empty string.

## Comments
Single line comment
```html
<!-- Single line comment -->
```

Multi-line comment
```html
<!-- Start here
  -- Multi line comment 
  -- More comment 
  -->
```

Closing element comment
```html
<aside class="sidebar">
    Sidebar stuff goes here
</aside><!-- end .sidebar -->
```