# Design-Web-Pages-with-CSS

## What is CSS

In the previous module, we learned how HTML uses different features such as headers, which will look larger than regular text, how paragraphs break onto a new line and have space between them, and how links are a different color, to distinguish them from normal text. In HTML these features are known as default styles, which are very basic styles that the browser applies, to make sure that it's basically readable, even if no explicit style is specified by the author. The browser styles HTML documents in an internal style sheet. With CSS you can control exactly how these HTML elements will look in the browser.  

CSS stands for Cascading Style Sheets, and it's a language that specifies how documents are presented, styled, and laid out to users. Other things that CSS is used for in basic document text styling include changing the color and size of headings and links, creating a layout from a single column of text, into a layout with a main content area, and a sidebar for related information. CSS can also be used for animation. 

### CSS syntax

CSS is a rules based language. Specifically, this means that you define the rules specifying groups of styles that should be applied to a particular element, or groups of elements on your web page. For example, if you want the main heading on your page to be shown as large red text, you would write it in CSS as:

h1 {
    color: red;
    font-size: 5em;
}

-You would first select the element you're going to style, in this example, it's an HTML header.

-You would then use the set of curly braces { } , and inside these curly braces would be the declarations, which take the form of property and value pairs. These property value pairs specify a property of elements, and the value we'd like to give the property.

-In the example above, before the colon we have the property (color)(font size), and after the colon we have the value (red)(5em). 

CSS style sheets can have the rules written one after the other. For example,

h1 {
    color: red;
    font-size: 5em;
}

p {
    color: black;
}

### CSS Modules

The CSS language is broken down into modules. For example, you could take a look at the [Backgrounds and Borders](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Backgrounds_and_Borders) module to find out what its purpose is, and what different properties and features it contains. 

### CSS Specifications
