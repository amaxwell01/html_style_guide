HTML Style Guide
================
A dedicated style guide for clean, consistent and standards based HTML


## Rules:
1. Avoid div-itis and use new HTML tags such as (header, footer, aside, article, section)
2. Avoid the use of ID's except for when needed by JavaScript. You never know when you will need to re-use a style,
or adapt a style for another use.
3. Don't code for yourself, code for others

## White Space
* Indent using soft tabs set to 4 spaces, don't use hard tabs.
```html
    <div class="container">
    ∙∙∙∙<h1>Header</h1>
    </div>
```

* Leave a single empty line between separate blocks of code
```html
    <div class="container">
        <h1>Header</h1>
    </div>

    <aside class="sidebar">
        <ul>
            <li>Sidebar</li>
        </ul>
    </aside>
```


## Doc Type:
Ensure that all websites use the new HTML5 doctype
```html
<!doctype html>
```

## Meta Tags:
### Character set
Ensure that all websites use UTF-8 character sets so that the pages can be read universally
```html
<meta charset="utf-8"> 
```
### Mobile / Responsive
Make sure to include a viewport meta tag when building a responsive or mobile dedicated website
<https://developer.mozilla.org/en-US/docs/Mobile/Viewport_meta_tag>
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

## Tags:
Use the HTML <button> element when ever you are linking to elements (not content) on the same page when 
you are not using anchor tags to link to content. This is ideally used when opening up modals, dialogs.

```html
<button>Your Button</button>
```

## Menus
When coding a menu, it is important to wrap your menu items with the new HTML5 <nav> tag. Since navigation links are 
usually a list of links, it is important to place the menu items in a list.

###General Menu
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

###Organized Menu
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

### Quotes:
When writing HTML in any language, you should always use double quotes for opening and closing attributes
```html
<button id="make_it_rain">Make it Rain</button>
```

### id="" / data-:
* Do not create overly complicated ID's which will be split and parsed to capture information, 
instead use 2 data- attributes. This will not only improve the JavaScript code used to parse the
information, it will also ensure that you or someone else who reads it "knows" exactly the reasoning
behind the code.
* Only use ID's when they are needed for JavaScript or singular elements, not for variable collection

###BAD
```html
<div id="basketball_20"></div>
```

###GOOD
```html
<div data-sport="basketball" data-player-number="20"></div>
```

### alt="":
All images which are using the <img> tag should use the alt attribute. If not alternative is provided, it is still 
recommended to use the alt attribute but with an empty string.

### onclick="":
When assigning the onclick event handler to any HTML element do not use the HTML attribute onclick="".
Instead use JavaScript or jQuery to attach the event handler to your object. There will always be some use cases where it will make sense to use the onclick="" attribute, but try to avoid them if possible.

####HTML
```html
<button id="make_it_rain">Make it Rain</button>
```
####JavaScript/jQuery
```javaScript
  var rainButton = $('#make_it_rain');

  rainButton.on('click', function() {
      console.log('Throw money!');
  });
```


## Comments
###Single line comment
```html
<!-- Single line comment -->
```

###Multi-line comment
```html
<!-- Start here
  -- Multi line comment 
  -- More comment 
  -->
```

###Closing element comment
```html
<aside class="sidebar">
    Sidebar stuff goes here
</aside><!-- end .sidebar -->
```