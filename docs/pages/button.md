# Button

<p class="uk-text-lead">Easily create nice looking buttons, which come in different styles.</p>

## Usage

To apply this component, add the `.uk-button` class and a modifier such as `.uk-button-default` to an `<a>` or `<button>` element. Add the `disabled` attribute to a `<button>` element to disable the button.

```html
<a class="uk-button uk-button-default" href=""></a>

<button class="uk-button uk-button-default"></button>

<button class="uk-button uk-button-default" disabled></button>
```

```example
<p uk-margin>
    <a class="uk-button uk-button-default" href="#">Link</a>
    <button class="uk-button uk-button-default">Button</button>
    <button class="uk-button uk-button-default" disabled>Disabled</button>
</p>
```

**Note** If you are displaying a number of buttons in a row, you can add a top margin to them, when they stack on smaller viewports. Just add the `uk-margin` attribute from the [Margin component](margin.md) to their parent element.

***

## Style modifiers

There are several style modifiers available. Just add one of the following classes to apply a different look.


| Example | Class | Description |
| --- | --- | --- |
| <button class="uk-button uk-button-default" type="button">Default</button> | `.uk-button-default` | Default button style. |
| <button class="uk-button uk-button-primary" type="button">Primary</button> | `.uk-button-primary` | Indicates the primary action. |
| <button class="uk-button uk-button-secondary" type="button">Secondary</button> | `.uk-button-secondary` | Indicates an important action. |
| <button class="uk-button uk-button-danger" type="button">Danger</button> | `.uk-button-danger` | Indicates a dangerous or negative action. |
| <button class="uk-button uk-button-text" type="button">Text</button> | `.uk-button-text` | Applies an alternative, typographic style. |
| <button class="uk-button uk-button-link" type="button">Link</button>| `.uk-button-link` | Makes a `<button>` look like an `<a>` element. |


***

## Size modifiers

Add the `.uk-button-small` or `.uk-button-large` class to a button to make it smaller or larger.


```html
<button class="uk-button uk-button-default uk-button-small"></button>

<button class="uk-button uk-button-default uk-button-large"></button>
```

```example
<p uk-margin>
    <button class="uk-button uk-button-default uk-button-small" type="button">Small button</button>
    <button class="uk-button uk-button-primary uk-button-small" type="button">Small button</button>
    <button class="uk-button uk-button-secondary uk-button-small" type="button">Small button</button>
</p>

<p uk-margin>
    <button class="uk-button uk-button-default uk-button-large" type="button">Large button</button>
    <button class="uk-button uk-button-primary uk-button-large" type="button">Large button</button>
    <button class="uk-button uk-button-secondary uk-button-large" type="button">Large button</button>
</p>
```

***

## Width modifier

Add the `.uk-width-1-1` class from the [Width component](width.md) and the button will take up full width.

### Example

```example
<button class="uk-button uk-button-default uk-width-1-1 uk-margin-small-bottom" type="button">Button</button>
<button class="uk-button uk-button-primary uk-width-1-1 uk-margin-small-bottom" type="button">Button</button>
<button class="uk-button uk-button-secondary uk-width-1-1" type="button">Button</button>
```

***

## Button group

To create a button group, add the `.uk-button-group` class to a `<div>` element around the buttons. That's it! No further markup needed.

```html
<div class="uk-button-group">
    <button class="uk-button uk-button-default"></button>
    <button class="uk-button uk-button-default"></button>
    <button class="uk-button uk-button-default"></button>
</div>
```

```example
<div>
    <div class="uk-button-group">
        <a class="uk-button uk-button-secondary" href="#">Link</a>
        <button class="uk-button uk-button-secondary">Button</button>
        <button class="uk-button uk-button-secondary">Button</button>
    </div>
</div>

<div class="uk-margin-small">
    <div class="uk-button-group">
        <a class="uk-button uk-button-primary" href="#">Link</a>
        <button class="uk-button uk-button-primary">Button</button>
        <button class="uk-button uk-button-primary">Button</button>
    </div>
</div>

<div>
    <div class="uk-button-group">
        <a class="uk-button uk-button-danger" href="#">Link</a>
        <button class="uk-button uk-button-danger">Button</button>
        <button class="uk-button uk-button-danger">Button</button>
    </div>
</div>
```

***

## Button with dropdowns

A button can be used to trigger a dropdown menu from the [Dropdown component](dropdown.md).

```html
<!-- A button toggling a dropdown -->
<button class="uk-button uk-button-default"></button>
<div uk-dropdown></div>
```

```example
<div class="uk-inline">
    <button class="uk-button uk-button-default">Dropdown</button>
    <div uk-dropdown>
        <ul class="uk-nav uk-dropdown-nav">
            <li class="uk-active"><a href="#">Active</a></li>
            <li><a href="#">Item</a></li>
            <li class="uk-nav-header">Header</li>
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
            <li class="uk-nav-divider"></li>
            <li><a href="#">Item</a></li>
        </ul>
    </div>
</div>
```

***

### Button group with dropdowns

Use button groups to split buttons into a standard action on the left and a dropdown toggle on the right. Just wrap the toggling button and the drop or dropdown inside a `<div>` element and add the `.uk-inline` class from the [Utility component](utility.md)

```html
<!-- A button group with a dropdown -->
<div class="uk-button-group">
    <button class="uk-button uk-button-default"></button>
    <div class="uk-inline">

        <!-- The button toggling the dropdown -->
        <button class="uk-button uk-button-default"></button>
        <div uk-dropdown="mode: click; boundary: ! .uk-button-group; boundary-align: true;"></div>

    </div>
</div>
```

```example

<div class="uk-button-group">
    <button class="uk-button uk-button-default">Dropdown</button>
    <div class="uk-inline">
        <button class="uk-button uk-button-default"><span uk-icon="icon:  triangle-down"></span></button>
        <div uk-dropdown="mode: click; boundary: ! .uk-button-group; boundary-align: true;">
            <ul class="uk-nav uk-dropdown-nav">
                <li class="uk-active"><a href="#">Active</a></li>
                <li><a href="#">Item</a></li>
                <li class="uk-nav-header">Header</li>
                <li><a href="#">Item</a></li>
                <li><a href="#">Item</a></li>
                <li class="uk-nav-divider"></li>
                <li><a href="#">Item</a></li>
            </ul>
        </div>
    </div>
</div>
```
