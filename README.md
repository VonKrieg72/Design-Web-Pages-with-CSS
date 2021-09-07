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

All web standard language code (HTML, CSS, JavaScript, etc) are defined in documents called specifications (or specs), which are published by organizations such as [W3C](https://developer.mozilla.org/en-US/docs/Glossary/W3C), [WHATWG](https://developer.mozilla.org/en-US/docs/Glossary/WHATWG), [ECMA](https://developer.mozilla.org/en-US/docs/Glossary/ECMA), or [Khronos](https://developer.mozilla.org/en-US/docs/Glossary/Khronos), and these organizations define how these technologies are suppose to behave. CSS was developed by [CSS Working Group](https://www.w3.org/Style/CSS/), which is a group within the W3C.

### Browser Support Information

Once CSS has been specified, then it's only useful for us in developing web pages if one or more browsers have implemented it. What this means is that the code has been written to turn the instruction in our CSS file into something that can be put on the screen. 

## How to Add CSS

There are three ways to insert a style sheet

-External CSS

-Internal CSS

-Inline CSS

### External CSS

If you want to change the look of an entire website, you can do so, by changing just one file with an External Style Sheet. Each HTML page must include a reference to the external style sheet file inside the < link > element, inside the head section. Below is an example of External styles, which are defined within the < link > element, inside the < head> section of an HTML page.

< !DOCTYPE html>

< html>

< head>

< link rel="stylesheet" href="mystyle.css">

< /head>

< body>

< h1>This is a heading< /h1>

< p>This is a paragraph.< /p>

< /body>

< /html>

An external style sheet can be written in any text editor, and must be saved with a .css extension. The external .css file should not contain any HTML tags.

### Internal CSS

In the event that one single HTML page has a unique style, then an internal style sheet may be used. The internal style is defined inside the < style> element, inside the head section.

< !DOCTYPE html>
< html>
< head>
< style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
} 
< /style>
< /head>
< body>

< h1>This is a heading</h1>
< p>This is a paragraph.</p>

< /body>
< /html>

### Inline CSS

If you need to apply a unique style for a single element, then an Inline Style may be used. In order to use Inline Styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.

< !DOCTYPE html>
< html>
< body>

< h1 style="color:blue;text-align:center;">This is a heading</h1>
< p style="color:red;">This is a paragraph.</p>

< /body>
< /html>

### Multiple Style Sheets

If some properties have been defined for the same selector (element) in different style sheets, the value from the last read style sheet will be used.

h1 {
  color: navy;
}

h1 {
  color: orange; 
  }

If the internal style is defined after the link to the external style sheet, the < h1> elements will be orange
  
  < head>
< link rel="stylesheet" type="text/css" href="mystyle.css">
< style>
h1 {
  color: orange;
}
< /style>
< /head>  

However, if the internal style is defined before the link to the external style sheet, the < h1> elements will be navy

< head>
< style>
h1 {
  color: orange;
}
< /style>
< link rel="stylesheet" type="text/css" href="mystyle.css">
< /head>

## CSS Color Property

The color property in CSS specifies the color of text. You should set the text color for different elements.

body {
  color: red;
}

h1 {
  color: #00ff00;
}

p.ex {
  color: rgb(0,0,255);
}

If you would like to look at a complete list of possible color values, then you can look at the [CSS Color Values](https://www.w3schools.com/cssref/css_colors_legal.asp).

An initial sets the property to its default value. If you would like to read more about an initial you can look at [Read about initial](https://www.w3schools.com/cssref/css_initial.asp)

An inherit inherits its property from its parent element. If you would like to read more about inherit, you can read about it at [Read about inherit](https://www.w3schools.com/cssref/css_inherit.asp).

## CSS Reference

Below is a basic rules syntax for CSS:

style-rule ::=
    
    selectors-list {
      
      properties-list
    }
    
    ...where:
    
    selectors-list ::=
    
    selector[:pseudo-class] [::pseudo-element]
    
    [, selectors-list]

properties-list ::=
    
    [property : value] [; properties-list]
    
 
 If you would like an alphabetical index of all the standard CSS properties, you can click on [CSS Alphabetical Index](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#index).
 
 ## CSS Tool: Reset CSS
 
 The reset stylesheet was created with the goal of reducing browser inconsistencies in things like default line heights, margins and font sizes of headings. Reset styles quite often appear in CSS frameworks. The reset styles examples below are very generic, and are meant as a starting point, which can be tweaked if you choose to do so.  
 
 * http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
