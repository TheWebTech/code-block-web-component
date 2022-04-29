# code-block-web-component
A code block web component and HubSpot module that leverages the component.

## How to use the web component
Wherever you want to place your code block you use HTML.

There are two elements in use.
### Code block element `<code-block>`

This is a wrapper element which contains `<code-tab>` elements. Multiple `<code-tab>` elements can be placed inside of a code block. This element generates tabs for each of the `<code-tab>` elements placed within it, and handles toggling the visibility of the individual tabs.

### Code tab element `<code-tab>`
This is the element that renders the syntax highlighted code itself. This element is designed to be used inside of `<code-block>` elements.

The code tab has three attributes:
* language - determines the which syntax highlighting is used.
* label - The label for the tab
* is-escaped - by default is-escaped is false. This attribute determines whether the module will convert any HTML inside the element to escaped HTML. You should never pass HTML that isn't already escaped. The HTML will be temporarily rendered.

Each of these attributes are passed as data attributes since these are custom attributes.
``` html
<code-tab data-language="HTML" data-is-escaped="false" data-label=" Rendered HTML">
    <h1>Your HTML here. Any HTML or HubL should be escaped</h1>
</code-tab>
```

### how they are used together
Example of how you'd use this:
``` html
    <code-block data-line-numbers="true">
        <code-tab data-language="HTML">
            <h1>Your HTML here. Any HTML or HubL should be escaped</h1>
        </code-tab>
    </code-block>
```

   
   
