[*Demo and API Docs*](http://alijaya.github.io/iron-accordions/components/iron-accordions/)

# &lt;iron-accordions&gt;

`iron-accordions` is for layouting purpose. Used together with `iron-accordion`. *(Note the s)*

Example:

``` html
<iron-accordions>
  <iron-accordion>
    <h2 header>This is the Header</h2>
    <p>This is a paragraph</p>
    <p>And more paragraph here</p>
  </iron-accordion>
  <iron-accordion>
    <h2 header>Compound Header</h2>
    <p header>Yeah</p>
    <p>I don't like writing a documentation</p>
    <p>YEAH!!!</p>
  </iron-accordion>
<iron-accordions>
```

See [iron-accordion](#iron-accordion) for more information about `iron-accordion`.

`iron-accordions` extends the behavior of `Polymer.IronMultiSelectableBehavior`, so it could have `selected` attribute, `multi`, etc.

Example:

``` html
<iron-accordions multi selectedValue="[1]">
  <iron-accordion>
    <h2>You can open the content more than one</h2>
    <p>Some content</p>
  </iron-accordion>
  <iron-accordion>
    <h2>This thing is opened by default</h2>
    <p>Some content</p>
  </iron-accordion>
  <iron-accordion>
    <h2>Some another header</h2>
    <p>Some another content</p>
  </iron-accordion>
</iron-accordions>
```

So if you want to init `iron-accordion` to be opened in the first time, you should set the property of `selected` from the `iron-accordions` (or `selectedValue` if `multi` is `true`).

**Don't** give the attribute `opened` *manually* to the `iron-accordion` because the data model in `iron-accordions` can't detect it.

## &lt;iron-accordion&gt;

`iron-accordion` is using [`iron-collapse`](https://github.com/PolymerElements/iron-collapse) for collapsing the content.
Currently, it will collapsing vertically.

The child element of `iron-accordion` with `[header]` attribute will be clickable button to reveal its content. *So it's advised not to include button or another interactive element for the header.*

Example:

``` html
<iron-accordion>
  <h2 header>This is clickable element to reveal the content</h2>
  <p>All the other thing beside the first element is the content</p>
  <button>Like this button</button>
  <span>Or this span</span>
</iron-accordion>
```

Bad Usage Example:

``` html
<iron-accordion>
  <button header>If you use interactive thing like this</button>
  <h2>It's really bad :(</h2>
  <p>Please don't do it...</p>
</iron-accordion>
```
