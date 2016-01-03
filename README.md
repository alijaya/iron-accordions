[*Demo and API Docs*](http://alijaya.github.io/iron-accordions/components/iron-accordions/)

# &lt;iron-accordions&gt;

`iron-accordions` is for layouting purpose. Used together with `iron-accordion`. *(Note the s)*

Example:

``` html
<iron-accordions>
  <iron-accordion>
    <h2>This is the Header</h2>
    <p>This is a paragraph</p>
    <p>And more paragraph here</p>
  </iron-accordion>
  <iron-accordion>
    <div>
      <h2>Compound Header</h2>
      <p>Yeah</p>
    </div>
    <p>I don't like writing a documentation</p>
    <p>YEAH!!!</p>
  </iron-accordion>
<iron-accordions>
```

See [iron-accordion]() for more information about `iron-accordion`.

`iron-accordions` extends the behavior of `Polymer.IronMultiSelectableBehavior`, so it could have `selected` attribute, `multi`, etc.

## &lt;iron-accordion&gt;

`iron-accordion` is using [`iron-collapse`](https://github.com/PolymerElements/iron-collapse) for collapsing the content.
Currently, it will collapsing vertically.

The first child element of `iron-accordion` will be clickable button to reveal its content. *So it's advised not to include button or another interactive element for the first child element.*

Example:

``` html
<iron-accordion>
  <h2>This is clickable element to reveal the content</h2>
  <p>All the other thing beside the first element is the content</p>
  <button>Like this button</button>
  <span>Or this span</span>
</iron-accordion>
```

Bad Usage Example:

``` html
<iron-accordion>
  <button>If you use interactive thing like this</button>
  <h2>It's really bad :(</h2>
  <p>Please don't do it...</p>
</iron-accordion>
```
