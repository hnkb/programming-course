
# HTML


## Basics

HTML is a markup language that describes content (web pages that include text, forms, graphics, menus, ...).
HTML only describes the content, and is not concerned with how the content is going to be displayed. Later,
we will use CSS style sheets to customise how HTML pages are presented.

See https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics for details.

### HTML syntax

An HTML page contains a tree of nested _elements_. Each element can contain text or other elements.

Summary:
  - Each element has a _start tag_ and an _end tag_.
  - Element content is placed between start and end tag
  - Element content can be text or other (nested) elements
  - Each element can have multiple _attributes_
  - Element names (types) and attributes are predefined by HTML standard
  - There is a special notation for empty elements (elements without any content).
    This notation can only be used with certain element types that can never have any content, like
    `<img />`, `<hr />` and `<br />`
  - As with any computer language, comments (text that compters ignore) can be  
  - HTML Comments: anything between comment start tag `<!--` and end tag `-->` will be ignored
  - Multiple whitespaces are ignored as well. No matter how many spaces, tabs, endline charaters you type,
    all of them will only mean "next word" and represented by a single space



### Anatomy of an HTML page

This is the template of an (empty) HTML page:

```html
<!DOCTYPE html>

<html>
<head>
    <meta charset="utf-8" />
    <title></title>
    
</head>
<body>

</body>
</html>
```

Forget about the first line (`<!DOCTYPE html>`), that's an irregular standard requirement for
backwards-compatibility. The document consists of:

  - one `<html>` element. This root elemnt contains:
      - one `<head>` element which contains description of the page (like its title, the style
        it should be presented in, page description, etc.), none of which is visible to the viewer.
        All of this information is for browsers and search engines.
      - one `<body>` element which contains everything visible in the page

Note: as with any computer language, we indent nested elements. This way, nesting relationships
can be easily identified with a glance.


## Important HTML elements

Three are three types of HTML tags:

 1. **[Inline elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)**:
    these elements do not affect text flow, and only affect their content. They can only contain text
    and other inline elements. The more useful ones include:
    
      - Text formatting and markup: [`<strong>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong),
        [`<em>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em),
        [`<b>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b),
        [`<i>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i),
        [`<time>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time),
        [`<abbr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr),
        [`<q>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q)

      - Link to other pages: [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)
        Link target is specified in `href` attribute.
        
      - Multimedia elements: [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img),
        [`<video>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video),
        [`<audio>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio),
        [`<svg>`](https://developer.mozilla.org/en-US/docs/SVG_In_HTML_Introduction),
        [`<canvas>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas),
        [`<object>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object)
        
      - Line break [`<br />`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br)
      
      - Inline text sectioning: [`<span>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span)
        `<span>` does not change the behaviour of its content, it just groups them so they can be treated
        as a unit when applying styles or manipulating the element programmatically.
        
      - Form elements, for getting user input:
        [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input),
        [`<button>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button),
        [`<textarea>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea),
        [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) and
        [`<option>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option),
        [`<label>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label).
        For details and samples of using forms, refer to
        [HTML Standard](https://developers.whatwg.org/forms.html#forms).
        
 2. **[Block elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)**:
    these elements denote a block of text, and therefore affect text flow. A block of text starts in a new
    line and is has its separate vertical space.
    
      - a normal paragraph is denoted with [`<p>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p).
        Paragraphs can only contain text and inline elements, no block elements can be inside a `<p>` element.
      
      - different levels of heading [`<h1>` to `<h6>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h1%E2%80%93h6).
        Headings, like parapraphs, can only contain text and inline elements, not block elements.
      
      - document outline (separating different parts of document) can be done with
        [`<div>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div) elements. `<div>` elements
        can contain any other element, block or otherwise.
        
        There are some more outlining elements, they behave like `<div>` but have special use-cases:
        [`<article>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article),
        [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section),
        [`<nav>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav),
        [`<aside>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside),
        [`<header>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header),
        [`<footer>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer),
        [`<main>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main),
        [`<address>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address),
        [`<blockquote>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote)
        
      - Lists can be created using [`<ul>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)
        for un-ordered lists (bullets), or [`<ol>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)
        for ordered lists (numbering). `<ul>` and `<ol>` elements can only contain
        [`<li>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li) elements and nothing else.
        Each `<li>` denotes one item of the list. `<li>` itself can contain any element, block or inline.
        
      - Tables can be created with
        [`<table>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table),
        [`<tr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr),
        [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td),
        [`<th>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th),
        [`<thead>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead),
        [`<tbody>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody),
        [`<tfoot>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot)
        
      - 

 3. **Metadata**: elements like [`<title>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
    and [`<meta>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) go into `<head>` and
    describe the page to machines (like browsers and search engines). They are not visible.

### Common attributes

  - **[`id`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id)**
    Defines a unique identifier for the element. For example:
    
    ```html
    <body>
        <h1 id="chapter-1">Chapter 1</h1>
        <p>...</p>
        
        <h1 id="chapter-2">Chapter 2</h1>
        <p>...</p>
    </body>
    ```
    
    In the above example, the `<h1>` element for chapter 2 is assigned a unique identifier and can be refered
    to as `#chapter-2`. If this was saved as `book.html`, we could link to the second chapter like this:
    `book.html#chapter-2`.
    
  - **[`class`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class)**
    attribute allows you to group similar elements. Giving the same class name to different elements does not
    have any visible effect, but we can write specific style sheet rules that are only applied to elements if
    they belong to a certain class; or we can write program code (in Javascript) that manipulates only those
    elements belonging to a certain class.
    
    Unlike `id` which is unique, the same class name can be assigned to multiple elements. An element can be
    assigned to multiple classes as well, just separate different class names with space character.
    
    ```html
    <ul>
        <li class="city capital">London</li>
        <li class="city">Liverpool</li>
        <li class="city capital">Tehran</li>
        <li class="mount">Everest</li>
    </ul>
    ```
    
    In the above example, London is assigned both `city` and `capital` class names, and belongs to both groups.
    
  - **[`dir`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)**
    specifies the direction of text. `ltr` for languages that are written from left to right (like English) and
    `rtl` for languages written from right to left (like Persian).


## References

  - https://developers.whatwg.org/
  - https://developer.mozilla.org/en-US/docs/Web/HTML
