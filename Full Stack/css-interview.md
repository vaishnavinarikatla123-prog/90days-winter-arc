                                # Day 2 – CSS Basics 

## 1. What is CSS?

**CSS (Cascading Style Sheets)** is used to style and design HTML elements. It controls the **appearance, layout, colors, spacing, fonts, and overall presentation** of a web page.

### Why is CSS necessary in Full Stack Development?

HTML is mainly used to create the **structure** of a webpage, while CSS is used to make that webpage **visually appealing, readable, responsive, and user-friendly**.

For example:

- HTML → creates a button
- CSS → gives the button color, size, spacing, border, etc.

---

## 2. Ways to Apply CSS

There are three main ways to apply CSS to HTML.

### A. Inline CSS

CSS is written directly inside the `style` attribute of an HTML element.

```html
<p style="color: blue;">Hello World</p>
```

Here, the style is applied only to that particular `<p>` element.

**Use:** Useful for applying a quick style to a specific element, but not preferred for large projects.

---

### B. Internal CSS

CSS is written inside the `<style>` tag in the HTML document, usually inside the `<head>`.

```html
<head>
    <style>
        p {
            color: blue;
        }
    </style>
</head>
```

This CSS can style multiple elements within the same HTML page.

**Use:** Useful when the styling is specific to a single HTML page.

---

### C. External CSS

CSS is written in a separate `.css` file and linked to the HTML file.

**HTML:**

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

**style.css:**

```css
p {
    color: blue;
}
```

### Why is external CSS preferred?

It separates **structure from presentation**, makes the code easier to maintain, and allows the same CSS file to be reused across multiple HTML pages.

---

# 3. How to Link an External CSS File

We use the `<link>` element inside the `<head>` of the HTML document.

```html
<link rel="stylesheet" href="style.css">
```

### Meaning:

- `link` → connects an external resource to the HTML document
- `rel="stylesheet"` → tells the browser that the linked file is a CSS stylesheet
- `href="style.css"` → specifies the location of the CSS file

---

# 4. CSS Color Property

The `color` property is used to change the **text color** of an element.

```css
p {
    color: red;
}
```

It can also use different color formats:

```css
p {
    color: blue;
}
```

```css
p {
    color: #0000ff;
}
```

```css
p {
    color: rgb(0, 0, 255);
}
```

---

# 5. CSS Background-Color Property

The `background-color` property is used to set the **background color** of an element.

```css
div {
    background-color: yellow;
}
```

### Difference:

```css
color: red;
```

→ Changes the **text color**.

```css
background-color: red;
```

→ Changes the **background color**.

---

# 6. What are CSS Selectors?

A **CSS selector** is used to select the HTML element(s) to which CSS styles should be applied.

Example:

```css
p {
    color: blue;
}
```

Here, `p` is the **selector**.

---

# 7. Types of CSS Selectors Learned

## A. Universal Selector

The universal selector is represented by `*`.

It selects **all elements**.

```css
* {
    color: red;
}
```

This applies the style to all elements.

---

## B. Element Selector

An element selector selects HTML elements based on their tag name.

```css
p {
    color: blue;
}
```

This selects all `<p>` elements.

Another example:

```css
h1 {
    color: green;
}
```

This selects all `<h1>` elements.

---

## C. Class Selector

A class selector is represented using `.` followed by the class name.

HTML:

```html
<p class="text">Hello</p>
```

CSS:

```css
.text {
    color: blue;
}
```

A class can be applied to **multiple elements**.

---

## D. ID Selector

An ID selector is represented using `#` followed by the ID name.

HTML:

```html
<p id="heading">Hello</p>
```

CSS:

```css
#heading {
    color: red;
}
```

An ID is generally intended to identify a **unique element** within a page.

---

# 8. What is CSS Specificity?

**CSS specificity determines which CSS rule is applied when multiple rules target the same element and property.**

For the normal selectors learned today, the priority is:

**Inline > ID > Class > Element > Universal**

### Example:

```html
<p id="text" class="para" style="color: red;">
    Hello
</p>
```

```css
#text {
    color: blue;
}

.para {
    color: green;
}

p {
    color: yellow;
}

* {
    color: black;
}
```

The text will be **red** because the inline style has higher priority than these normal selector rules.

### Specificity order:

| Selector | Example | Priority |
|---|---|---|
| Inline | `style="..."` | Highest |
| ID | `#text` | ↓ |
| Class | `.text` | ↓ |
| Element | `p` | ↓ |
| Universal | `*` | Lowest |

**Important:** `!important` can override normal specificity rules, so it should be treated separately rather than simply added to this list.

---

# 9. Key Things I Learned Today

- HTML provides the **structure** of a webpage.
- CSS provides the **style and presentation**.
- CSS can be applied using **inline, internal, or external CSS**.
- External CSS is useful for maintaining reusable and organized styles.
- `color` changes the **text color**.
- `background-color` changes the **background color**.
- CSS selectors determine **which HTML elements are styled**.
- CSS specificity determines **which applicable rule takes precedence** when multiple rules target the same property.


                       ----DAY 3/90 WINTER ARC CHALLENGE----

# CSS Text Properties

CSS text properties are used to control the **appearance, alignment, spacing, and transformation of text** on a webpage.

---

## 1. `text-decoration`

The `text-decoration` property is used to add or remove decorative lines from text.

### Common values:

- `underline` → adds a line below the text
- `overline` → adds a line above the text
- `line-through` → adds a line through the text
- `none` → removes text decoration

### Example:

```css
a {
    text-decoration: none;
}
```

This removes the default underline from a link.

### Interview answer:

> `text-decoration` is used to add or remove decorative lines such as underline, overline, and line-through from text.

---

## 2. `text-align`

The `text-align` property is used to specify the **horizontal alignment of text** inside an element.

### Common values:

- `left`
- `right`
- `center`
- `justify`

### Example:

```css
h1 {
    text-align: center;
}
```

This places the text in the center of the element.

### Interview answer:

> `text-align` is used to control the horizontal alignment of text within an element.

---

## 3. `font-weight`

The `font-weight` property controls the **thickness or boldness of text**.

### Common values:

```css
font-weight: normal;
font-weight: bold;
```

It can also use numeric values such as:

```css
font-weight: 400;
font-weight: 700;
```

Generally:

- `400` → normal
- `700` → bold

### Example:

```css
h1 {
    font-weight: 700;
}
```

### Interview answer:

> `font-weight` is used to control how thick or bold the text appears.

---

## 4. `font-size`

The `font-size` property controls the **size of the text**.

### Example:

```css
p {
    font-size: 20px;
}
```

Here, the paragraph text will have a size of `20px`.

### Interview answer:

> `font-size` is used to specify the size of text.

---

## 5. `font-family`

The `font-family` property specifies the **typeface or font** used to display text.

### Example:

```css
body {
    font-family: Arial, sans-serif;
}
```

Here, the browser tries to use `Arial`. If Arial is unavailable, it can use another `sans-serif` font.

### Interview answer:

> `font-family` is used to specify the font type or typeface for text.

---

## 6. `line-height`

The `line-height` property controls the **vertical space between lines of text**.

### Example:

```css
p {
    line-height: 1.5;
}
```

A larger line-height makes the lines more spread out, which can improve readability.

### Interview answer:

> `line-height` is used to control the vertical spacing between lines of text.

---

## 7. `text-transform`

The `text-transform` property controls the **capitalization of text**.

### Common values:

- `uppercase` → converts text to uppercase
- `lowercase` → converts text to lowercase
- `capitalize` → capitalizes the first letter of each word
- `none` → keeps the original text

### Example:

```css
h1 {
    text-transform: uppercase;
}
```

If the HTML contains:

```html
<h1>Hello World</h1>
```

It will appear as:

```text
HELLO WORLD
```

### Interview answer:

> `text-transform` is used to control the capitalization of text without changing the actual HTML content.

---

# CSS Box Model

## What is the CSS Box Model?

The **CSS Box Model** describes how every HTML element is represented as a rectangular box and how its **content, padding, border, and margin** determine its size and spacing.

The four parts of the CSS Box Model are:

```text
Content
   ↓
Padding
   ↓
Border
   ↓
Margin
```

---

## 1. Content

The **content** is the actual area containing the text, image, or other content of an element.

Example:

```css
div {
    width: 200px;
    height: 100px;
}
```

The `width` and `height` normally define the content area when using the default `content-box` box sizing.

---

## 2. Padding

**Padding** is the space between the content and the border.

```css
div {
    padding: 20px;
}
```

Padding creates space **inside** the element.

Think:

> Content → Padding → Border

---

## 3. Border

The **border** surrounds the padding and content.

```css
div {
    border: 2px solid black;
}
```

A border can have a width, style, and color.

---

## 4. Margin

**Margin** is the space outside the border. It creates space between the element and surrounding elements.

```css
div {
    margin: 20px;
}
```

Margin creates space **outside** the element.

---

# Padding vs Margin

This is a common interview question.

### Padding

> Space **inside** the element, between the content and border.

### Margin

> Space **outside** the element, between the border and surrounding elements.

Example:

```css
div {
    padding: 20px;
    margin: 30px;
}
```

Here:

- `20px` → space inside the element
- `30px` → space outside the element

---

# Why is the Box Model Important?

The CSS Box Model is important because it helps us understand and control the **size, spacing, and layout of elements** on a webpage.

It is especially useful when creating responsive and well-structured layouts.

---

# Box Model Structure

```text
┌───────────────────────────────┐
│            Margin             │
│   ┌───────────────────────┐   │
│   │        Border         │   │
│   │   ┌───────────────┐   │   │
│   │   │    Padding    │   │   │
│   │   │  ┌─────────┐  │   │   │
│   │   │  │ Content │  │   │   │
│   │   │  └─────────┘  │   │   │
│   │   └───────────────┘   │   │
│   └───────────────────────┘   │
└───────────────────────────────┘
```

### Easy way to remember:

**Content → Padding → Border → Margin**

- **Content** → actual content
- **Padding** → space inside
- **Border** → boundary around the element
- **Margin** → space outside